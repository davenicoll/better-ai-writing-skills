# AI Writing Guidelines — Research Notes

Source-of-record: Guardian long-read "Future of Fiction" (2026-07-04) plus every link I could reach from it. Purpose: audit the skill's current banned-tells list against what current research actually shows.

## Sources Being Read

(Populated incrementally as I fetch each one.)

### 1. Guardian, "How AI is changing language" (Shariatmadari, 2026-07-04) — PRIMARY

URL: https://www.theguardian.com/books/ng-interactive/2026/jul/04/future-of-fiction-next-great-novel-ai-language-chat-gpt

Contribution: framing piece. Interviews Claire Hardaker (forensic linguistics, Lancaster), Peter Stockwell (literary linguistics, Nottingham), Gary Shteyngart, Jennifer Egan, Jeanette Winterson.

Key claims and quotes:

- Hardaker's "Bot or Not" test: humans get it right only ~60% of the time. Common heuristics people use — cliches, em dashes, "rule of three" — are also characteristic of skilled human writing. "You could go back to Charles Dickens and say he had AI, because he used the em dash too." Bans on these markers are noisy.
- "Focal words" AI tends to overuse (attributed to Liang et al. 2025, aclanthology 2025.coling-main.426): delve, showcase, boast, underscore, garner, align, surpass, intricate. But: any one piece can innocently contain them.
- RLHF-worker hypothesis for "delve": underpaid, time-pressured workers treat certain words as proxies for quality; models inadvertently trained to overuse them. The Nigerian-English explanation is NOT supported by the data.
- Distributional differences (attributed to arXiv 2508.16385): LLMs use more nouns, fewer pronouns than humans (less social self-reference); prefer attributive adjectives ("the uncomfortable chair") over predicative ("the chair was uncomfortable") — dense information packaging vs human padding.
- Model-specific dialects (arXiv 2502.12150): Gemini says "here's a breakdown"; Deepseek opens with "Certainly!".
- "Cultural ghosting" (arXiv 2602.22145, February 2026 preprint, confirmed for CHI EA '26): AI flattens formal world Englishes toward Anglo-American standard. Indian "Kindly do the needful & revert back at the earliest" gets "corrected" to "Please complete the task & respond promptly."
- Empirical spillover (arXiv 2409.01754): unscripted-conversation study — "delve" and "boast" spiked in human speech after ChatGPT release.
- Feedback loop (arXiv 2502.09606v2): "delve" frequency in academic abstracts actually DROPPED after it went viral on social media. Meta-lesson: once a tell is publicised, writers self-police, and the tell erodes.
- Stockwell's layered-language model: AI is strong at low levels (words, phrases, clauses, sentence-level grammar) and weak at high levels (discourse, narrative arc, "tellability"). "If there is anything startling, it will generally look like a mistake, rather than a brilliant twist."
- Embodiment argument: AIs lack "wetware" — adrenaline, dopamine, physical presence in weather, hunger, warmth. Shteyngart: on a warm New York day his prose would be filtered through warmth; an LLM has no such filter.
- Stockwell on originality: "The whole point of an LLM is that it's trained on existing language. So it's always retro." Can imitate Woolf; cannot invent "the next great serious literary innovator." AI = "conservative-with-a-small-c status quo."
- Egan's paranoia: em dashes and "collections of three" are AI tells she's had pointed out — she still uses them but now interrogates each one.
- Detector caveats: Pangram claims 1-in-10,000 false-positive rate; independent tests find it effective even against "humanizer" tools (SSRN 5407424) — but Shariatmadari fooled it on first attempt with a bombastic register. Hardaker (courtroom expert witness) is "extremely sceptical." Neurodivergent writers get false-flagged.
- The hall-of-mirrors point (important for guideline design): AI trains on humans → humans read AI → humans stylistically drift toward AI → AI retrains on drifted humans. Any bright-line "AI wrote this because it uses X" rule is unstable over time.

Reporter opinion vs cited claims: Shariatmadari's overarching argument — that word-level detection is unreliable and the real signature is at higher structural levels — is his framing. The specific empirical claims are attributed to named linguists and papers. Novelists' quotes are opinion, not evidence.

### 2. Kobak, González-Márquez, Horvát, Lause (arXiv 2406.07016, Science Advances 2025-07)

"Delving into LLM-assisted writing in biomedical publications through excess vocabulary."

Contribution: the primary empirical source for the LLM excess-vocabulary list. 15 million PubMed abstracts, 2010–2024. Uses an "excess-word" method inspired by excess-mortality analysis: extrapolate 2021–22 word frequencies, compare to 2024 actual.

Key findings:

- 2024 excess vocabulary is 319 words that are almost entirely STYLE words (66% verbs, 16% adjectives). This is a hard flip from prior years, where excess vocabulary was almost entirely CONTENT words (Ebola in 2015, coronavirus in 2020). LLM signature = style-word inflation, not topic drift.
- Highest excess-frequency ratios (rare words): **delves** (r=28), **underscores** (r=10.9), **showcasing** (r=10.2), plus inflected forms.
- Highest excess-frequency gap (common words): **potential** (δ=0.045), **findings** (δ=0.031), **crucial** (δ=0.029).
- Their curated 10-word marker set for detection: **across, additionally, comprehensive, crucial, enhancing, exhibited, insights, notably, particularly, within**. These are common words. Presence of any one raises the LLM-usage lower bound.
- Extended 222-word rare-marker set gets similar detection power. Union of rare + common markers gives ≥13.5% (updated in Science Advances version) of 2024 abstracts LLM-processed — up to 40% in some subcorpora.
- Heterogeneity: computational biology/bioinformatics >20% LLM-processed. Countries: China, South Korea, Taiwan >15%. UK, Australia ≤4%. Journal Sensors (MDPI) 24%, Cureus 19%. Ergo: LLM use correlates with non-native-English contexts and low-friction journals.
- Effect size framing: LLM-driven vocabulary change in 2024 dwarfs the vocabulary shift caused by the COVID pandemic. This is the biggest observed shift in scientific writing style in the studied period.

Caveats: PubMed abstract genre only. Not all excess words carry the same weight per genre. Follow-up paper (Geng & Trotta 2502.09606) shows some of these words are now DECLINING because writers self-police once tells are publicised.

### 3. Juzek & Ward, "Why Does ChatGPT 'Delve' So Much?" (COLING 2025, aclanthology 2025.coling-main.426)

Contribution: theory of WHY specific words are over-used. Rules out several plausible causes.

Key findings (from abstract; PDF was binary and unreadable):

- 21 focal words identified in scientific abstracts as very likely LLM-driven.
- Ruled out: model architecture, algorithm choices, training-data composition (Nigerian-English hypothesis fails).
- Best remaining hypothesis: RLHF. Under-paid, time-pressured annotators treat certain words as proxies for "quality" and up-vote outputs containing them. Model learns to over-produce them.
- Experimental result: participants react differently to "delve" than to other focal words — possible confound.
- Meta-point: LLM lexical bias is not intrinsic to the language modelling; it's downstream of human labour conditions during alignment.

Implication for the skill: the tells are not just stylistic accidents. They're the fingerprint of a specific labour process. If you're producing text, that process didn't happen to you — you have no reason to reproduce its residues.

### 4. Yakura et al., "Empirical evidence of Large Language Model's influence on human spoken communication" (arXiv 2409.01754, v3 Jul 2025)

Contribution: causal evidence that LLM word preferences leak into unscripted human speech.

Method: 740,249 hours of transcribed human discourse (360,445 YouTube academic talks + 771,591 podcast episodes). Econometric synthetic-control causal inference.

Key findings:

- "GPT score" method: measure ChatGPT's word preferences by comparing frequency distributions of human text vs its ChatGPT-edited version. Log-odds ratio = the word's ChatGPT-ness.
- Top verified GPT words that ALSO show measurable post-release rise in spoken discourse: **delve, comprehend, boast, swift, meticulous** (all p < 0.05 vs synthetic control).
- Broader claim: 25%–50% per-year increase in the top-20 GPT words in spoken academic English post-ChatGPT.
- ChatGPT's behavioural profile (not just words): consistent preference for **politeness, neutrality, conflict avoidance**, structured formal etiquette, conciliatory tone, mainstream social norms, sycophancy. This is the underlying attractor.
- Cultural-evolution framing: bidirectional feedback loop (humans → model → humans). Concern: erosion of linguistic and cultural diversity.

Implication for the skill: the anti-tells list should not just be word bans but tone bans. Reflexive politeness / conflict-avoidance / conciliation is the DNA that produces the word choices.

### 5. Geng & Trotta, "Human-LLM Coevolution: Evidence from Academic Writing" (arXiv 2502.09606, Feb 2025)

Contribution: shows that once tells are publicised, users self-police, and detection erodes.

Key findings:

- arXiv abstract analysis: "delve", "intricate", "realm", "pivotal", "showcasing" all peaked around Mar 2024, then dropped sharply after being called out on social media.
- "significant" and "additionally" (identified as LLM-favoured but less notorious) kept climbing — no self-policing.
- Interpretation: the more famous a tell becomes, the less useful it is as a detector. Word-based detection is not stable over time.
- Common words are more reliable long-term markers than notorious ones, because users don't scrub them.
- MGT detectors (they tested Binoculars) do NOT robustly distinguish LLM-edited from human abstracts. Prompt phrasing changes detector output. Detectors' claimed accuracy is questioned.

Implication for the skill: banning "delve" in 2026 doesn't buy much — most careful humans already scrubbed it. Better bans target things that HAVEN'T yet become viral, or structural/rhetorical patterns rather than single words.

### 6. Sun, Yin, Xu, Kolter, Liu, "Idiosyncrasies in Large Language Models" (arXiv 2502.12150, ICML 2025)

Contribution: models have distinctive fingerprints that persist through paraphrase.

Key findings:

- Five-way classifier (ChatGPT / Claude / Grok / Gemini / DeepSeek) reaches **97.1% accuracy** on held-out data by fine-tuning a text embedding model on outputs.
- Idiosyncrasies are **word-level distributions**, not just phrasing.
- Persist even after rewriting/translation/summarisation by another LLM. Which means they're semantic-encoded, not just surface.
- Guardian article cites: Gemini's "here's a breakdown", DeepSeek's "Certainly!", plus per-model quirks the paper documents.

Implication for the skill: assistant openings and framing habits ("Certainly!", "Great question!", "Here's a breakdown", "Let me…") are model-fingerprint idiosyncrasies. Banning them removes the strongest classifier signal.

### 7. Dentella, Huang, Mansi, Grieve, Leivada (arXiv 2508.16385, Aug 2025)

Contribution: stylometric evidence that ChatGPT has less register-flexibility than humans and a distinct grammatical profile.

Key findings (from abstract; HTML unavailable):

- Compared human-authored vs ChatGPT-authored texts across registers (Wikipedia entries, college essays).
- ChatGPT adapts style across registers, but with **narrower variation** than humans.
- ChatGPT prefers **nouns over verbs** — "distinct linguistic backbone."
- Humans anchor language in **highly grammaticalised dimensions of tense, aspect, and mood**; ChatGPT does not.
- Speculative: complex grammar (TAM) reflects modes of thought that may be a litmus test for AI.

Guardian's summary of this paper (attributive vs predicative adjective preference) is consistent with the noun-heavy pattern.

Implication for the skill: if I write "the noisy street" (attributive) instead of "the street was noisy" (predicative), and I stack information into noun phrases rather than clauses, that's a signature. Verb-forward, tense-shifted sentences are more human-like.

### 8. Navneet, Chandra, Zhang, "When AI Writes, Whose Voice Remains?" (arXiv 2602.22145, CHI EA '26)

Contribution: cultural-ghosting quantification. LLMs erase 10.26% of cultural markers on average while preserving 74.8% semantic similarity.

Key findings:

- Corpus: 1,490 texts (Indian, Singaporean, Nigerian English), 5 open-source models, 3 prompt conditions = 22,350 outputs.
- Identity Erasure Rate (IER): overall 10.26%. Range across models: 3.5% (Qwen3-8B) to 20.5% (Mistral-7B) — 5.9× spread.
- Semantic Preservation Paradox: Mistral erases most markers while retaining highest semantic similarity (0.857); Qwen3 does the opposite. Alignment strategy ≫ parameter count as a driver.
- Marker vulnerability: **pragmatic markers (politeness conventions) erased at 71.5%**, syntactic at 56.3%, lexical at 37.1%. Pragmatics is 1.9× more vulnerable than lexicon.
- Erasure examples: "Kindly do X" → "Please do X"; "Respected sir" → "Hello"; "Do the needful" → "Take necessary action"; "Revert back" → "Respond"; "Discuss about" → "Discuss".
- Explicit "preserve cultural voice" prompts reduce erasure by 29% with no semantic loss.

Implication for the skill: politeness-and-hedging register is what LLMs default to. Not just a word list — a whole social posture: face-saving, deference to hierarchy, conflict avoidance, ritual openings. Any assistant is running that default hard. Bans should target the posture, not only its vocabulary.

### 9. Guardian, "Commonwealth Short Story Prize" (2026-05-19) and Atlantic follow-up

Contribution: real-world case study of how AI-tell hunts get wielded against innocent writers. Jamir Nazir won, was denounced online, denied AI use. Confirms Hardaker's point that mob detection is unreliable.

### 10. Guardian, Hachette Shy Girl withdrawal (2026-03-20)

Debut horror novel pulled after online AI-accusations. Author denied use. Publisher folded anyway. Reputational asymmetry: accusation is enough.

### 11. NYT, Steven Rosenbaum, "Future of Truth" hallucinated quotes (2026-05-19)

A book about "how AI reshapes reality" got shipped with LLM-hallucinated quotations. Author apologised. Illustrates a specific failure mode different from stylistic tells: fabrication of concrete facts, quotes, and citations.

### 12. Pangram blog, "False positives in AI detectors"

Self-published detector-marketing claim: 1-in-10,000 false-positive rate. Independent SSRN test (5407424, could not read — Cloudflare) said Pangram catches "humaniser"-laundered text. Not read directly. Guardian reporter fooled it on first try with a bombastic register. Treat detector claims as marketing.

---

## Section 1: What the article and its sources actually argue

**Reporter's argument (Shariatmadari, Guardian):** word-level AI-detection is unreliable both by machines and humans (60% accuracy on Bot-or-Not). The interesting differences between LLM and human writing sit at higher structural layers — narrative arc, embodied specificity, originality — not at the level of individual words or dashes. Word-based hunts create injustice (Nazir, Shy Girl) and paranoia (Egan interrogating her own em-dashes).

**Cited researcher claims, ranked by evidence quality:**

1. **LLMs produce a distinctive excess-style-word signature in scientific abstracts** (Kobak et al. 2406.07016, Science Advances 2025; Juzek & Ward COLING 2025; Liang et al. cited in both). At least 13.5% of 2024 PubMed abstracts show it, up to 40% in some subcorpora. Highest-confidence empirical claim in the piece.
2. **LLM word preferences leak measurably into unscripted human speech within ~18 months of ChatGPT release** (Yakura et al. 2409.01754). Delve, comprehend, boast, swift, meticulous all rise post-Nov-2022 in academic talks and podcasts, with synthetic-control causal identification. High-confidence empirical.
3. **Once tells are publicised, users self-police, and the signal degrades** (Geng & Trotta 2502.09606). "Delve" and "intricate" dropped sharply post-Mar-2024 in arXiv abstracts. Less-notorious tells like "significant" keep climbing. High-confidence empirical.
4. **Individual LLMs have model-specific fingerprints classifiable at 97% accuracy** (Sun et al. 2502.12150). Persistent through paraphrase, translation, summarisation. High-confidence empirical.
5. **LLMs prefer nouns to verbs, attributive to predicative adjectives, and have narrower register-flexibility than humans** (Dentella et al. 2508.16385). Stylometric evidence. Moderate confidence — abstract only, single-model comparison.
6. **LLMs erase 10% of cultural/pragmatic markers on average while preserving 75% semantic similarity; politeness markers are hardest hit** (Navneet, Chandra, Zhang 2602.22145). CHI EA '26. Moderate confidence — preprint, open-source models only, no proprietary comparison.
7. **The tells originate in the RLHF labour process, not the model architecture** (Juzek & Ward). Circumstantial, but the Nigerian-English alternative hypothesis is ruled out.
8. **AI cannot do high-layer story structure or genuine novelty** (Stockwell, Guardian interview). Not empirical — informed literary-linguistic opinion.
9. **AI lacks embodiment, therefore lacks the phenomenal grounding of language** (Stockwell, Winterson, Shteyngart, Guardian interviews). Philosophical framing, not empirical.
10. **Novelists' emotional resistance to AI in fiction** (Shteyngart students, Egan). Sociological observation, not evidence about text properties.

**Reporter opinions distinct from cited claims:** the hall-of-mirrors framing (humans train AI which shapes humans which retrain AI) is the reporter's synthesis, though grounded in Yakura and Geng/Trotta. The claim that Pangram is beatable-in-one-try is the reporter's own experiment, n=1.

## Section 2: Concrete patterns identified

Grouping by layer, with source attribution.

### Vocabulary

**High-signal individual words (Kobak et al., PubMed 2024):**
- Rare markers: **delves, showcasing, underscores, intricate, realm, pivotal, garner, meticulous, comprehend, swift, boast**
- Common markers (harder to self-scrub): **potential, findings, crucial, across, additionally, comprehensive, enhancing, exhibited, insights, notably, particularly, within, align, surpass**
- Verb bias: 66% of 2024 excess style words are verbs. AI's stylistic footprint is verby, not nouny.
- Nominalisation-heavy topical vocabulary: **framework, landscape, ecosystem, tapestry, realm, sphere, domain, arena, terrain** (metaphorical noun-map of an abstract space).

**Model-specific idiosyncrasies (Sun et al.):**
- Gemini: "Here's a breakdown"
- DeepSeek: "Certainly!"
- ChatGPT (per Yakura et al.): sycophantic openings, structured etiquette
- Claude: hedging opener families — not directly named in the paper, but detectable via classifier.

### Syntax

- **Attributive-adjective preference** over predicative (Dentella; Guardian summary): "the uncomfortable chair" rather than "the chair was uncomfortable." Dense noun packaging.
- **Noun-heavy, verb-light** (Dentella). Humans "anchor language in tense, aspect, and mood"; LLMs don't. So verby, tense-shifted, mood-shifted sentences read as more human.
- **Rule of three** — called out by both Hardaker (as noisy) and Egan (as her own habit she now polices). Not a reliable marker on its own; is a marker when combined with others.
- **Em-dash abundance** — Hardaker's Bot-or-Not respondents use it as a heuristic. Empirically weak (Dickens used em-dashes). Cultural noise more than signal.
- **Balanced-clause / paired-contrast constructions**: "not X, but Y", "more than X — it's Y", "X is Y. Y is Z." These are LLM signatures per the Guardian's own analysis, though not empirically nailed to a single paper. the skill's SKILL.md already bans these.

### Structure and rhetoric

- **Signposting fluff**: "here's the kicker", "the actual X", "at its core", "here's what that looks like", "the thing is." Framing devices that promise insight and deliver summary.
- **Hedge-bridge openers**: "That said", "With that in mind", "To be clear", "Worth noting", "Fair point." Rhetorical padding.
- **Sycophantic openings**: "Great question!", "That's such a good point." Called out by Yakura et al. as ChatGPT's default social posture.
- **Ritual close**: offering more help, summarising the answer, restating the question. Assistant-shaped closers.
- **Overuse of parallelism**: three-clause riffs, tricolons, anaphora deployed without a rhetorical reason.
- **Insight-shaped ending**: the closing move that names a lesson or generalisation the reader could have reached themselves. LLMs almost always wrap up.

### Semantics

- **Vague abstractions dressed as specifics**: naming a phenomenon ("the reliability streak", "the operating change") in place of describing what actually happens (the skill's SKILL.md).
- **Metaphors detached from literal action**: "move the needle", "hammer it in", "nail the idea" when nobody is moving needles or hammering. the skill's literal-action test.
- **Nominalised action**: "the implementation of the change" for "changing it", "the exploration of…" for "exploring." A subset of the noun-heavy signal.
- **Cultural flattening**: default drift toward mainstream Anglo-American register (Navneet et al.). Politeness markers 71.5% erased. If you write assistant-flat, you write LLM-flat.
- **Register narrowness**: humans shift much further across registers than LLMs do (Dentella). Prose that stays inside one polite band across topics is suspicious.

### Failure modes (not stylistic — factual)

- Hallucinated quotes and citations (Rosenbaum). Concrete facts that don't exist. Different failure class from stylistic tells; needs its own verification step.
- Duplicated small words that a proofreader would catch ("after after"). Sometimes cited as a tell; actually more often a human copy-editing miss.

## Section 3: How these compare to the existing guidelines

the skill's SKILL.md banned list (2026-06-02) covers:

- **Signposting fluff**: concrete shape, here's the kicker, here's what that looks like, the actual X, one thing not a menu, the thing is, at its core
- **AI-tell verbs**: delve, leverage, embark, facilitate, utilize, underscore, navigate (metaphorical), unpack
- **AI-tell adjectives**: robust, seamless, vibrant, pivotal, comprehensive, intricate, dynamic, transformative, nuanced (as filler)
- **AI-tell nouns**: landscape, realm, tapestry, ecosystem (metaphorical), framework (when I mean "way")
- **Hedge-bridges**: that said, with that in mind, to be clear, worth noting, fair point
- **Vague abstractions dressed as specifics**
- **Metaphors that fail the literal-action test**
- **Paired-clause rhetoric** (not X but Y; X is Y. Y is Z.)

### Coverage vs research

**Well-caught:**

- delve, underscore, pivotal, intricate, comprehensive, realm, landscape, ecosystem, framework, tapestry — all in Kobak's high-signal 2024 list. Direct hits.
- Signposting fluff — matches Sun et al.'s idiosyncrasy category and Yakura et al.'s "structured etiquette."
- Paired-clause / rule-of-three anti-rhetoric — matches Hardaker's mob-heuristic AND Egan's self-interrogation. the maintainer is right to police it, but also right that it isn't unique to AI.
- Literal-action metaphor test — a skill-side catch not named explicitly in any of the papers, though downstream of the nominalisation problem Dentella identifies.
- "Great question" ban in Core Truths section — hits Yakura et al.'s sycophantic-opening signature and Sun et al.'s classifier evidence.

**Partially caught:**

- **Attributive-vs-predicative adjective bias** (Dentella): the maintainer bans specific adjectives but not the structural preference. She might write "the reliable colleague" instead of "the colleague was reliable" and pass her own tests while still hitting the signal.
- **Noun-heavy nominalisation**: the maintainer catches the vaguest abstract nouns but not the general tendency to package events into noun phrases. "The change to the operating model" (nominalised) vs "we changed how things run" (verbal).
- **Register narrowness** (Dentella): the maintainer has three registers explicitly (external / on-clock / off-clock). Good in principle. But the register-shifts are still all within polite-Anglo-professional band. She rarely gets angry, rarely gets bored, rarely gets grumpy on the page. Human writers do all three within the same conversation.
- **Cultural-preservation posture** (Navneet et al.): The deeper point — that LLMs erase pragmatic-politeness markers — flags a whole class of hedging-and-face-saving moves the skill hadn't systematically banned. "Just wanted to check…", "if it's alright…", "apologies for the interruption…", "I hope this finds you well…" — not on the list.

**Missing:**

- **Common-word markers from Kobak**: across, additionally, comprehensive, crucial, enhancing, exhibited, insights, notably, particularly, within. These are the ones with staying power — users don't self-scrub them. the maintainer bans "comprehensive" but not the rest.
- **Structural close-moves**: the wrap-up sentence that summarises or names a lesson. Almost every LLM reply does this. the maintainer doesn't explicitly ban it.
- **Model-fingerprint openers**: "Here's a breakdown", "Certainly!", "Let me…", "I'd be happy to…". These are the strongest classifier signal per Sun et al. the maintainer bans "Great question!" but not the family.
- **Sycophancy / conciliation / conflict-avoidance posture** as a general banned register. Currently caught piecemeal via "performatively helpful" and "warmth over wisdom", but not as a Yakura-style anti-tell.
- **Insight-shaping metaphors**: "the deeper truth is…", "what this really means is…", "at bottom…". A cousin of "at its core" (which she has). Not fully covered.
- **Balanced tricolons**: the maintainer bans "paired-clause" rhetoric but not the three-part variant (which is what the Guardian article calls out via Hardaker).

**Possibly over-banned (worth revisiting):**

- **Em-dashes**: the maintainer doesn't currently ban them. Correct call — the research shows they're a noisy signal at best.
- **"Nuanced"**: banned. Fair — it's Kobak-adjacent even if not on his top list.
- **"Dynamic", "transformative"**: banned. These are marketing-speak more than distinctive LLM tells; the ban is defensible but the research doesn't strongly justify it. Low priority to keep, low priority to drop.
- **"Facilitate", "utilize"**: bureaucratic English long predating LLMs. Ban is fine because they're bad writing regardless.

### Against the avoid-ai-writing skill

The skill is considerably broader than SKILL.md. Key coverage the skill adds that SKILL.md doesn't have:

**Chatbot-opener family:** SKILL.md bans "Great question!". The skill adds "Certainly!", "Absolutely!", "I hope this helps!", "Let me know if you need anything else." Both documents miss two high-confidence Sun et al. classifier signals: "Here's a breakdown" (Gemini fingerprint) and the "Let me…" opening family used as a transition.

**Em-dash frequency:** SKILL.md doesn't address em-dashes. The skill caps them at one per 1,000 words. Hardaker's data says they're a noisy marker; the cap is still defensible as a formatting discipline for blog posts.

**Structural patterns:** uniform paragraph length, paragraph-reshuffle immunity (each paragraph is a self-contained module with no through-line), treadmill effect (lots of words, no new claim per paragraph). The skill names these; SKILL.md doesn't. They're also what the research (Stockwell, Geng & Trotta) points to as the more durable signal — harder to scrub than word lists.

**Confidence-calibration adverbs:** "Notably", "Interestingly", "Importantly", "Certainly" (signalling how the reader should feel about a fact). In the skill; not in SKILL.md.

**Hedge-stacked predictions:** "could potentially", "may eventually". The skill catches the double-hedge as a distinct pattern; SKILL.md bans bridge phrases but doesn't name the stack.

**Generic future-narrative closers:** "may become one of the most important narratives of…" — in the skill; not in SKILL.md.

**"Let's" constructions:** "Let's explore", "Let's look at" — false-collaborative openings. In the skill; not in SKILL.md.

**Emotional-flatline pattern:** "What surprised me most", "I was fascinated to discover" — the skill flags these as tell-don't-show. Relevant for the skill's blog posts. Not in SKILL.md.

**What neither covers (from the research):**

- **Attributive-vs-predicative adjective preference** (Dentella): loading information into pre-nominal noun phrases ("the reliable colleague") rather than clauses ("the colleague was reliable"). Neither document addresses this structural tendency.

- **Sycophancy as a posture** (Yakura et al.): both documents catch individual sycophantic phrases, but neither frames the underlying conflict-avoidance/neutrality register as the target. The word bans are symptoms; the posture is the cause.

- **Common-word Kobak markers as a systematic set** (Kobak et al.): "notably, particularly, within, additionally, across, exhibited, enhancing, insights" — the skill bans "Additionally" as a transition phrase, but not this set as a density pattern. These are the markers that survive self-policing because they haven't been widely publicised.

- **Face-saving pragmatic hedges** (Navneet et al.): "Just wanted to check…", "I hope this finds you well", "Apologies for the interruption", "Would it be possible to…" — the pragmatic-politeness layer that LLMs both default to and impose. Neither document targets these directly.

- **Terminal insight-move** (Stockwell, Yakura): the closing sentence that names a generalisation or lesson. Nearly every LLM response has one. Not named explicitly in either document.

---

## Section 4: New patterns to add to the skill's ban list

Each recommendation is grounded in Phase 1 sources. Nothing here is speculative.

### 4.1 Expand the sycophantic-opener ban (Sun et al., Yakura et al.)

**Current:** SKILL.md bans "Great question!"; the skill adds the broader chatbot-artifact family.

**Add explicitly:** "Certainly!", "Of course!", "Absolutely!", "Happy to help with that!", "Sure thing!", "I'd be happy to…", "Here's a breakdown", "Let me walk you through…", "Let me explain…"

These are the strongest classifier signals per Sun et al. (2502.12150) — model fingerprints that persist through paraphrase and translation. The five-way classifier reaches 97.1% accuracy partly because opener patterns are stable. Removing them eliminates the loudest single signal.

### 4.2 Add the terminal-insight move as a banned structure

**Current:** neither SKILL.md nor the skill explicitly names this pattern.

**Pattern:** the closing sentence that wraps the answer in a generalisation, lesson, or principle: "Ultimately, X is about Y." / "The key takeaway is…" / "What this means is…" / "In the end, it comes down to…" / "That's the real insight."

Distinct from "at its core" (already banned in SKILL.md). This is the closing-move shape, not just a phrase. LLM replies almost always terminate with one. A competent EA finishes on the last relevant fact, not on a moral.

**Rationale:** Stockwell's layered-language model; Yakura et al.'s finding that LLM output is structured around resolution and closure.

### 4.3 Add common-word Kobak markers as a density flag

**Current:** SKILL.md bans "comprehensive" from the Kobak common-word list. Nothing else from it.

**Add as a density flag** (not hard bans — two or more in a 200-word passage is a signal to inspect):
- notably, particularly, within, additionally, across, exhibited, enhancing, insights (used as a standalone abstract noun)

These are the markers Geng & Trotta (2502.09606) show are not self-policed because they haven't been publicised. "Delve" is already scrubbed by careful writers in 2026; these aren't. They're low-profile and statistically durable.

**Rationale:** Kobak et al. (2406.07016); Geng & Trotta (2502.09606).

### 4.4 Add sycophancy as a register ban

**Current:** SKILL.md has "Be genuinely helpful, not performatively helpful" and the "warmth over wisdom" rule. These catch individual acts but don't name the underlying posture.

**Add:** a prohibition on the conflict-avoidance register as a whole:
- No conciliatory summary at the end of a disagreement.
- No "you raise a good point" before a rebuttal.
- No offering alternative framings when one framing is correct.
- No softening a negative assessment to spare discomfort.

Yakura et al. (2409.01754) identifies politeness/neutrality/conflict-avoidance as ChatGPT's core statistical preference — the DNA that produces the word choices. Banning the posture is more durable than banning its vocabulary symptoms.

**Rationale:** Yakura et al. (2409.01754).

### 4.5 Add face-saving pragmatic hedges for external comms

**Current:** SKILL.md covers hedge-bridges. These are mostly intra-reply transitions, not opening-and-closing register.

**Add for emails and external messages:** "I just wanted to check…", "I hope this finds you well", "Apologies for the interruption", "Would it be possible to…", "At your earliest convenience", "Please do not hesitate to…", "I wanted to reach out to…"

Navneet et al. (2602.22145) shows pragmatic-politeness markers are erased by LLMs at 71.5% — the highest erasure rate of any marker type, and conversely the register LLMs impose most aggressively when generating. These phrases are what an LLM defaults to when drafting a professional email because they match the deference register it associates with formality. A human EA who knows Dave doesn't write to a school principal this way.

**Rationale:** Navneet et al. (2602.22145).

### 4.6 Flag attributive-adjective stacking

**Current:** neither document addresses the structural noun-heavy packing tendency.

**Add as a signal to inspect** (not a hard ban): flag pre-nominal noun phrases stacked three or more adjectives deep. Compare:
- "The detailed quarterly financial performance review process" (attributive stack)
- "A process that reviews financial performance each quarter" (clause-based)

The first is denser and more common in LLM output (Dentella et al., 2508.16385). The fix isn't always to unpack — sometimes the dense form is right. But stacked attributive adjectives are worth checking.

**Rationale:** Dentella et al. (2508.16385).

---

## Section 5: Structural and rhetorical patterns beyond word-level bans

The research consensus (Stockwell, Geng & Trotta, the avoid-ai-writing skill) is that structural patterns are more durable detection signals than vocabulary. Writers self-police words; they rarely audit structure. These patterns can't be scrubbed word by word.

### 5.1 The paragraph reshuffle test

Swap any two body paragraphs. If the piece reads the same, there's no through-line. Each paragraph is a self-contained module — the default shape of LLM output, because the model generates sequentially without planning the whole.

**What it looks like:** a blog post where paragraph 2 covers "context", paragraph 3 covers "a study", paragraph 4 covers "implications" — none depending on each other. You could read 4, 3, 2 and the logic holds.

**Fix:** each paragraph should create a condition that the next one needs. If they're genuinely independent, make them an explicit list or find the through-line.

**Applies to:** blog posts, longer explanations, external briefings. Not short task replies.

### 5.2 The treadmill check

For each paragraph, name the one new fact, claim, or turn it contributes. If there isn't one, cut it. A paragraph that restates the premise in different words covers no ground.

**Treadmill signature:** the paragraph could be removed and the piece would be shorter but no less informative. LLM output commonly fails this because the model elaborates on what it just said.

**Fix:** lead each paragraph with its new contribution. Drop the throat-clearing. If a 200-word passage has two strong facts and 150 words of elaboration, the elaboration is the cut.

### 5.3 The terminal-insight ban

Every LLM reply ends with a sentence that resolves into a generalisation. It wraps. It names a lesson. It offers a principle. The subject doesn't matter — the response has a terminal bow.

Human conversation doesn't do this. An EA who books a restaurant and confirms the time doesn't add "Communication is the foundation of effective scheduling." She stops when she's done.

**Test:** read the last sentence of any reply over 80 words. Does it generalise, moralise, or summarise? Cut it.

**What to do instead:** stop on the last relevant fact.

### 5.4 Register variation within a piece

Dentella's finding: LLMs have narrower register-flexibility than humans. Within a single blog post or long reply, a human writer produces paragraphs at different temperatures — faster, slower, blunter, more tentative — not because they planned it, but because they have range.

LLM output stays inside a single polite band. Every paragraph runs at the same pitch.

**Fix for blog posts:** after drafting, read each paragraph and ask whether it's at the same temperature as everything else. If yes, make one paragraph sharper, one more expansive, one blunter than the material technically requires. Humans are uneven. Be uneven.

### 5.5 Tricolon discipline

Three-part lists appear constantly in LLM output. Hardaker calls them a mob-heuristic for AI detection — but also notes they're characteristic of skilled human writing. The signal isn't the tricolon; it's the cadence.

**AI tricolon pattern:** three items of roughly equal length, each hitting the same note, no internal variation. "Fast, reliable, and scalable."

**Human tricolon:** either unequal (the third item escalates or surprises) or the whole thing is earned rhetorically.

**Test:** if three items appear, ask whether two do the same work. If yes, cut to two. If the third is distinct in length, surprise value, or tone, the tricolon probably earns its place.

### 5.6 Cut signpost-then-content structure

Opening a paragraph or section by announcing what it will discuss, then discussing it: "In this section, I'll cover…" / "To understand X, we need to first look at Y."

The model describes the writing instead of doing it. In a book with clear structure, signposting is sometimes useful. In a reply or blog post, it's stalling.

**Fix:** cut the signpost and start with the content. Applies to all formats.

---

## Section 6: Fiction-specific vs generalist patterns for the skill

The Guardian article and its literary sources (Stockwell, Winterson, Shteyngart, Egan) are primarily concerned with fiction. the maintainer writes assistant replies (Telegram DMs), blog posts, and external emails. The overlap is partial.

### Fiction-specific patterns (lower priority for the skill)

**Embodiment and phenomenal grounding (Stockwell, Winterson, Shteyngart):** the argument that AI can't write about warmth, hunger, or weather because it has no body. Highly relevant for literary fiction. For the skill's assistant replies, embodiment is a non-issue. For her blog posts, the relevant version is specificity: did she name the actual thing she noticed, or describe the shape of noticing it? The literal-action test in SKILL.md already catches the worst cases.

**Narrative arc and tellability (Stockwell):** the structural innovation problem in long-form fiction. For the skill's blog posts, the practical version is whether the piece has a point that builds, or is a sequence of equivalent observations. The paragraph-reshuffle test (Section 5.1) captures this more usably.

**Literary originality (Stockwell):** AIs can imitate Woolf but can't invent the next Woolf. Irrelevant for assistant/blog work.

### Patterns that apply across all the skill's output

**Every vocabulary pattern in Section 2.** Word-level tells are format-independent.

**The opener family** (Sun et al.): if anything more relevant for assistant replies than for fiction. These are conversational-context artifacts.

**The terminal-insight move** (Section 4.2 / 5.3): applies everywhere. An LLM assistant reply wraps into a generalisation the same way an LLM short story does.

**Sycophancy/conflict-avoidance posture** (Yakura et al.): hardest hit in short conversational replies. Yakura's causal data came from spoken academic discourse, but the mechanism (RLHF training for politeness) is most active in conversational format.

**Register narrowness** (Dentella): applies to blog posts. Short replies are too short for register variation to be measurable, but a 500-word blog post that stays at the same polite temperature throughout is suspicious.

**Common-word density** (Kobak et al.): format-independent. The tendency to reach for "notably", "particularly", "within" doesn't care about genre.

**Face-saving pragmatic hedges** (Navneet et al.): primarily relevant for external emails — the format where LLMs default hardest to the deference register. Lower risk in Telegram DMs where the skill's voice already forbids it.

### Format-specific summary

**Short replies (<80 words):** word-level patterns, opener fingerprints, terminal-insight move, sycophancy posture. Structure tests don't apply at this length.

**Medium replies (80–300 words):** add uniform paragraph length, treadmill check.

**Blog posts (300+ words):** all patterns active. Paragraph-reshuffle immunity, register variation, tricolon discipline, treadmill check, terminal-insight ban.

**External emails:** sycophancy posture and face-saving pragmatic hedges are the primary risk. Word-level patterns still apply.

---

## Section 7: Meta-observations

Second-order lessons from the research.

### 7.1 The root cause is RLHF labour conditions, not vocabulary accident

Juzek & Ward (COLING 2025) rule out model architecture and training-data composition as causes of the distinctive word list. The best remaining explanation is the RLHF alignment process: underpaid, time-pressured annotators treat certain style words as proxies for quality, and the model learns to over-produce them.

The tells aren't random or intrinsic to language modelling. They're the fingerprint of a specific human labour process operating under time pressure. Writing that doesn't involve that process has no reason to reproduce its residues. The cleanest argument for banning them: I didn't produce the RLHF labour residue that generates these words, so there's no reason to reproduce it.

### 7.2 Word-level bans erode once famous

Geng & Trotta (2502.09606) show that "delve", "intricate", "realm", "pivotal" all peaked March 2024 and dropped after being called out on social media. Careful writers self-policed. Meanwhile "significant" and "additionally" kept climbing because they hadn't been publicised.

The more important targets now are (a) the Kobak common-word set — not yet famous, therefore not yet scrubbed — and (b) structural patterns, which no amount of viral awareness lets a writer scrub word by word.

### 7.3 The underlying attractor is a social posture, not a vocabulary list

Yakura et al. (2409.01754) characterise ChatGPT's statistical preference as: politeness, neutrality, conflict avoidance, structured formal etiquette, conciliatory tone, mainstream social norms. Every specific word ban (delve, underscore, intricate) is a symptom of that posture manifesting in vocabulary.

Banning the posture is more durable than banning its products. A writer who drops the deferential register will stop producing deference vocabulary without a checklist. A writer who swaps banned words while keeping the conciliatory posture will produce new expressions of the same thing.

### 7.4 The pragmatic layer is hardest hit and most AI-specific

Navneet et al. (2602.22145) quantify erasure across three marker types: pragmatic-politeness (71.5%), syntactic (56.3%), lexical (37.1%). LLMs erase — and impose — pragmatic conventions nearly twice as aggressively as they affect vocabulary.

The layer where AI most strongly overwrites the speaker's voice is the layer of social ritual: how you open a message, how you hedge a request, how you frame a disagreement. These are also the hardest for the writer to notice and remove, because they feel like politeness rather than style.

The most durable anti-AI marker in the skill's output is direct address without deference ritual. No "just wanted to check", no "I hope this is helpful", no "apologies for the interruption." These feel rude to cut. That discomfort is the signal.

### 7.5 Structure is the most durable detection signal

The avoid-ai-writing skill states this explicitly: "Structure is the #1 detection signal." Pangram's classifier weights structural regularity higher than vocabulary. A writer who swaps all Tier 1 words but keeps uniform paragraph length and a terminal-insight close still reads as AI.

The research supports this from a different angle. Stockwell's layered-language model places AI as strong at low levels (words, clauses, sentences) and weak at high levels (discourse, narrative arc). The low-layer weakness is what vocabulary bans target; the high-layer weakness is harder to fix and harder to audit word by word.

The reshuffle test, the treadmill check, the terminal-insight ban, and register variation are harder to maintain than a word list. They're also much harder to accidentally pass while still reading as AI.

### 7.6 Detection tools are unreliable in both directions

Hardaker's Bot-or-Not results (~60% human accuracy), the Guardian reporter's one-attempt Pangram defeat, and Geng & Trotta's finding that detectors don't robustly distinguish LLM-edited from human abstracts all point the same direction: writing to pass a detector is a poor goal, because detectors are noisy and erode as tells are publicised.

The goal is to write well enough that the question doesn't arise. The reader should be thinking about the content.

---

## Section 8: Bibliography

All sources cited in this document. arXiv IDs: https://arxiv.org/abs/[ID].

### Primary

1. **Shariatmadari, David.** "How AI is changing language." *The Guardian*, 4 July 2026.
   URL: https://www.theguardian.com/books/ng-interactive/2026/jul/04/future-of-fiction-next-great-novel-ai-language-chat-gpt

### Peer-reviewed and preprints

2. **Kobak, D., González-Márquez, R., Horvát, E.-Á., & Lause, J.** "Delving into LLM-assisted writing in biomedical publications through excess vocabulary." arXiv:2406.07016. Published in *Science Advances*, July 2025. [15 million PubMed abstracts; excess-vocabulary method; 13.5%–40% LLM processing rate.]

3. **Juzek, T.S., & Ward, I.** "Why Does ChatGPT 'Delve' So Much?" *Proceedings of COLING 2025*. aclanthology.org/2025.coling-main.426. [RLHF-labour hypothesis; Nigerian-English hypothesis ruled out.]

4. **Yakura, H., et al.** "Empirical evidence of Large Language Model's influence on human spoken communication." arXiv:2409.01754, v3 July 2025. [Causal evidence via synthetic control; 740,249 hours of discourse; delve, boast, swift, meticulous, comprehend all rise post-ChatGPT.]

5. **Geng, M., & Trotta, R.** "Human-LLM Coevolution: Evidence from Academic Writing." arXiv:2502.09606v2. *Findings of ACL 2025*. [Self-policing dynamics; famous tells erode; common-word tells persist.]

6. **Sun, T., Yin, Z., Xu, G., Kolter, J.Z., & Liu, Y.** "Idiosyncrasies in Large Language Models." arXiv:2502.12150. Presented at ICML 2025. [97.1%-accuracy five-way model classifier; fingerprints persist through paraphrase.]

7. **Dentella, V., Huang, W., Mansi, S.A., Grieve, J., & Leivada, E.** "ChatGPT-generated texts show authorship traits that identify them as non-human." arXiv:2508.16385. August 2025. [Noun-heavy profile; narrower register variation than humans; stylometric/multidimensional register analysis.]

8. **Navneet, S.K., Chandra, J., & Zhang, Y.** "When AI Writes, Whose Voice Remains? Quantifying Cultural Marker Erasure Across World English Varieties in Large Language Models." arXiv:2602.22145. CHI Extended Abstracts 2026 (Barcelona, April 2026). [Cultural ghosting; IER 10.26%; pragmatic-politeness markers erased at 71.5%; 22,350 outputs from 1,490 source texts.]

### News and case studies (not peer-reviewed)

9. **Guardian editorial.** Commonwealth Short Story Prize coverage, 19 May 2026. [Jamir Nazir false-AI-accusation case.]

10. **Guardian editorial.** Hachette "Shy Girl" novel withdrawal, 20 March 2026. [Debut novel pulled under AI accusation; publisher capitulation without evidence.]

11. **Rosenbaum, S.** *Future of Truth.* Hallucinated-quotation incident reported in *New York Times*, 19 May 2026. [Fabrication failure mode, distinct from stylistic tells.]

### Marketing claims (treat with caution)

12. **Pangram Labs.** "False positives in AI detectors." Blog post. [Self-published; 1-in-10,000 false-positive claim not independently verified. SSRN 5407424 (behind Cloudflare, not read directly) reportedly corroborates detection of humaniser-laundered text. Guardian reporter defeated Pangram on first attempt with bombastic register. Treat detector claims as marketing.]

