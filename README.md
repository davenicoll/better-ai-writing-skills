<div align="center">

# better-ai-writing-skills

**Audit and rewrite content to remove AI writing patterns.**

Detect / edit-in-place / iterate modes. Voice profiles. Research-grounded pattern list based on 2024–2026 stylometry literature.

Fork of [avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) by Conor Bronsdon (MIT), synced with upstream v3.34.0 and extended with the Guardian 2026-07-04 long-read pass — see [notes/2026-07-04-guardian-research-pass.md](notes/2026-07-04-guardian-research-pass.md) for the research the extensions are grounded in.

</div>

---

## What this is

A single [SKILL.md](SKILL.md) that audits and rewrites content to remove AI writing patterns ("AI-isms") — the vocabulary, syntax, structure, and posture patterns that make text sound machine-generated. Works standalone or as a plugin for Claude Code / Cowork.

Three modes:
- **`rewrite`** (default) — flag AI-isms and rewrite to fix them.
- **`detect`** — flag only. No rewriting. Useful for audits, published content, someone else's writing.
- **`edit`** — apply minimal, targeted edits to a file in place.

Optional voice profile (`casual` / `professional` / `technical` / `warm` / `blunt`) and context profile (`linkedin` / `blog` / `technical-blog` / `investor-email` / `external-email` / `docs` / `casual`). Iterate-to-convergence up to 2 passes.

## Upstream sync

The skill text tracks upstream. As of v3.12.0 (2026-09-12) it carries every SKILL.md rule change from upstream v3.11.0 through v3.34.0: the Tier 1A/1B split, 25 new pattern categories, the never-inject rewrite guardrails, and the voice-profile guardrail fixes. Upstream sections that depend on tooling this repo does not ship (quote normalizer, house-style config checker, preservation validator) were reduced to their tooling-free guidance. The deterministic detector under `detector/` and the Cursor rule are still at the v3.11 catalog and have not been synced.

## What this fork adds vs upstream

Six research-grounded categories from a July 2026 pass over the Guardian long-read "How AI is changing language" (Shariatmadari) and the primary papers it cites:

1. **Model-fingerprint openers** (Chatbot artifacts subsection) — the "Certainly!", "Here's a breakdown", "Let me walk you through" family that Sun et al. (arXiv:2502.12150, ICML 2025) show a five-way LLM classifier hits 97.1% accuracy on.

2. **Tier 4 — Second-wave density markers** — the Kobak et al. common-word set (`notably`, `particularly`, `within`, `additionally`, `across`, `exhibited`, `enhancing`, `insights`) that persists because it hasn't been publicised. Geng & Trotta (arXiv:2502.09606) show viral tells erode; silent ones climb.

3. **Sycophancy as a posture, not a vocabulary list** — Yakura et al. (arXiv:2409.01754) causal evidence that RLHF training produces a politeness/conflict-avoidance stance. Bans the structural moves that generate the vocabulary.

4. **Terminal-insight move** (structural test) — every LLM reply ends with a generalisation, moral, or principle. Explicit ban with a diagnostic test.

5. **Register variation within a piece** (300+ word diagnostic) — Dentella et al. (arXiv:2508.16385) show LLMs have narrower register-flexibility than humans. Test: are all paragraphs at the same temperature?

6. **Attributive-adjective stacking** (structural signal) — Dentella et al. also identify LLM preference for pre-nominal noun phrases over clauses.

7. **New context profile: `external-email`** — Navneet et al. (arXiv:2602.22145) quantify LLM erasure of pragmatic-politeness markers at 71.5%, and correspondingly show LLMs default hardest to a deference register in exactly this format. Face-saving pragmatic hedges as primary tell.

Plus a **Research basis appendix** documenting the primary literature behind every category, and two smaller additions from the same pass: a **tricolon-nuance refinement** to the existing rule of three, and an explicit **signpost-then-content structural pattern** at paragraph/section level.

## Install

### Claude Code (plugin)

```
/plugin marketplace add davenicoll/better-ai-writing-skills
/plugin install better-ai-writing-skills@davenicoll-skills
```

### Cowork desktop

**Customize → Plugins → Add marketplace from GitHub** → `davenicoll/better-ai-writing-skills`, then install **better-ai-writing-skills**.

### OpenClaw

```
git clone https://github.com/davenicoll/better-ai-writing-skills ~/.openclaw/skills/better-ai-writing-skills
```

### Manual (any agent)

Clone the repo and point your agent at `SKILL.md`:

```
git clone https://github.com/davenicoll/better-ai-writing-skills
```

Then reference `SKILL.md` from your agent config or drop it into your skills directory. The skill has no external dependencies — it's a single markdown file that the model reads and follows.

### Cursor rule

```
curl -o .cursor/rules/better-ai-writing.mdc \
  https://raw.githubusercontent.com/davenicoll/better-ai-writing-skills/main/cursor-rules/better-ai-writing.mdc
```

## Usage

Natural language triggers the skill. Some phrasings the skill recognises:

- "remove AI-isms from this"
- "clean up the AI writing in `draft.md`"
- "audit this post for AI patterns"
- "rewrite this in a blunt voice for LinkedIn"
- "make this sound less like AI, don't rewrite, just flag"
- "clean up `post.md` in place"

Power-user options (rarely needed — natural language usually works):
- `--mode rewrite|detect|edit`
- `--voice casual|professional|technical|warm|blunt`
- `--context linkedin|blog|technical-blog|investor-email|external-email|docs|casual`
- `--file PATH` (edit mode)
- `--iterate N` (max 2)
- `--style GUIDE` (best-effort named house style, no compliance claim)

## What's in the pattern list

The skill defines **80 pattern categories**. Tier 1 (always flag) and Tier 2 (flag in clusters) cover ~120 vocabulary entries. Tier 3 flags common words at density. Tier 4 (v3.11) adds the Kobak second-wave markers. Beyond vocabulary, the skill covers:

- Formatting (em dashes, bold, emoji, bullets, quotes)
- Sentence structure ("It's not X — it's Y", hollow intensifiers, hedging)
- Template phrases and transition phrases
- Structural issues (uniform paragraphs, missing bridges, paragraph-reshuffle immunity, treadmill effect)
- Rhetorical patterns (rule-of-three, generic conclusions, terminal-insight move, signpost-then-content)
- Register (sycophancy posture, register variation, attributive-adjective stacking)
- Chatbot artifacts (openers, tool markup leaks, acknowledgment loops)
- Conversational-register tells (wall-of-text replies, recap-flattery openers, narrated candor, lingering-attention claims)
- Rhetorical tics (performed-insight phrases, negation chains, same-opener runs, stranded auxiliary contrast, manufactured punchlines)
- Launch and social copy (dramatic introductions, fake-casual register, dramatized contrast against the crowd)
- Rewrite guardrails (the never-inject list: no fake first person, manufactured stakes, or invented specifics)
- Detection-tool caveats (what this skill isn't)

See [SKILL.md](SKILL.md) for the full list.

## Detection caveats

Every pattern in the skill is a **signal, not proof**. False-positive rates on non-native English writers exceed 60% in independent audits (Liang et al., Stanford, *Patterns* 2023). Adversarial paraphrase reduces detector accuracy by ~88% (arXiv:2506.07001, 2025). Hardaker's "Bot or Not" test shows humans achieve ~60% accuracy on the discrimination task and often rely on heuristics (em dashes, tricolons) that also appear in skilled human writing.

Use the skill as a writing-quality tool, not as a verdict machine. Pair the signal with context: who wrote it, what genre, what the writer's normal voice looks like. Don't ruin someone's day over it.

## Attribution

- **Original author:** [Conor Bronsdon](https://github.com/conorbronsdon) — [avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing), MIT licensed. Skill text synced through upstream v3.34.0.
- **Fork maintainer:** [Dave Nicoll](https://github.com/davenicoll) — v3.11 research-grounded extensions.

The upstream skill body is preserved, with the fork's extensions marked `(v3.11 addition)` inline and grounded in cited primary sources. See [SKILL.md](SKILL.md) § "Research basis" for the bibliography.

## Licence

MIT — same as upstream. See [LICENSE](LICENSE).

## Related

- Upstream: [conorbronsdon/avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing)
- Guardian long-read (2026-07-04): [How AI is changing language](https://www.theguardian.com/books/ng-interactive/2026/jul/04/future-of-fiction-next-great-novel-ai-language-chat-gpt)
