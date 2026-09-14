# Writing for Executives: Research Report

Prepared 2026-09-12 for the `better-ai-writing-skills` repo, to ground a proposed `executive` voice profile and `executive-deck` context profile.

Method: WebSearch + WebFetch across ~35 sources. Where a page returned 403/404 and I relied on a search-engine snippet or a secondary summary, the citation is marked **[unverified fetch]**. Direct quotations are from pages I fetched or PDFs I extracted with `pdftotext`. Nothing below is invented; where I could not confirm a widely-repeated claim I say so.

---

## 0. Executive summary (of the research itself)

- Every canonical framework converges on one rule: **state the answer first, then support it** (Minto's governing thought; military BLUF; Duarte's "summarize up front"; UK submissions "phrase advice so the Minister can just say yes or no"; Board Intelligence's "What am I asking of you?"). No source disagrees.
- Concrete length norms are remarkably consistent: **2–4 pages** for a decision paper or ministerial submission; **~6 pages** for an Amazon narrative (read in **20 minutes**); **15–20 words** average sentence length; slide titles **≤ 2 lines / ≤ 15 words**; **one message per slide**; **10% rule** for summary slides vs appendix.
- Empirical evidence: powerless-speech research (hedges, hesitations, tag questions) reduces perceived competence and even neutralizes strong arguments (Blankenship & Holtgraves 2005; Burrell & Koper 1998 meta-analysis). But Berger et al. (Wharton, 2024) show *some* hedges — high-likelihood + first-person ("I think this will likely…") — read as confident and persuade. Jargon measurably reduces processing fluency and information-seeking (Shulman et al. 2020; Bullock & Bisbey 2025) and receptivity to it correlates with worse analytical thinking (Littrell, Cornell 2026). Heavy AI assistance in managers' messages cuts perceived sincerity from 83% to 40–52% (Coman & Cardon 2025).
- Anti-patterns cluster into three families: (1) **padding/deference** ("I wanted to reach out", "please find attached", "as per", "just checking in"); (2) **consultant jargon** ("circle back", "synergy", "leverage", "low-hanging fruit", "bandwidth", "take this offline"); (3) **LLM tells** ("delve", "testament", "underscore", "it's important to note", negative parallelism, rule-of-three, em-dash clusters, "I hope this finds you well").
- Existing AI-writing skills (including this repo's SKILL.md and upstream `avoid-ai-writing`) handle business tone only via `professional`/`blunt` voices and an `investor-email`/`external-email` context. None has an executive-specific profile with BLUF, quantified-ask, decision-needed, or deck mechanics rules. That is the gap.

---

## 1. Canonical frameworks

### 1.1 Minto Pyramid Principle and SCQA

Source: Barbara Minto, *The Pyramid Principle*; summarised at [antoinebuteau.com/lessons-from-barbara-minto](https://www.antoinebuteau.com/lessons-from-barbara-minto/), [barbaraminto.com](https://www.barbaraminto.com/), [ModelThinkers](https://modelthinkers.com/mental-model/minto-pyramid-scqa), [Think Insights](https://thinkinsights.net/strategy/pyramid-principle).

Rules (quoted from the Buteau summary, which quotes Minto):
- "Ideas at any level must always be summaries of the ideas grouped below them."
- "Ideas in each grouping must always be the same kind of idea."
- Ideas in a grouping follow one of four orders: deductive, chronological, structural, comparative.
- Groupings limited to **3–7 points** (Buteau's paraphrase of Minto's "what the mind can easily process").
- Vertical logic: each summary connects upward. Horizontal logic: points at the same level align.
- Introduction = **SCQA**: Situation (something the reader already accepts as true) → Complication → Question → Answer (the governing thought at the apex).
- "Good ideas ought not to be dressed up in bad prose." Present messages "as starkly and simply as possible."
- Introduction rules: only content the reader will agree is true; the question may be implied.

Takeaway for the profile: answer first; 2–4 supporting arguments that are MECE and of the same kind; introduction restricted to agreed facts.

### 1.2 McKinsey / BCG / Bain deck conventions: action titles, horizontal and vertical logic

Sources: [Slideworks – action titles](https://slideworks.io/resources/how-to-write-action-titles-like-mckinsey) (fetched), [Poesius – how MBB structure final presentations](https://poesius.com/blog/how-mckinsey-bcg-bain-structure-final-presentations) (fetched), [Deckary – consulting slide standards](https://deckary.com/blog/consulting-slide-standards) (fetched), [MConsultingPrep – MBB slides](https://mconsultingprep.com/how-consultants-make-mbb-slides) (fetched), [Autopresent – McKinsey deck](https://www.autopresent.ing/blog/mckinsey-deck/), [Slidescience – action titles](https://slidescience.co/action-titles/).

Concrete rules:
- Title is a **full-sentence assertion**, not a label. "Revenue has declined 12% primarily due to volume loss" not "Revenue overview." (Poesius; Slideworks)
- **Length: "fit within one or max two lines, up to 15 words"; "NEVER have a title that is longer than two lines."** (Slideworks). Deckary independently: "Maximum 15 words", "Never exceed two lines".
- **Disagreement**: MConsultingPrep says an action title is "a short summary of about 5-6 words." This is the outlier; Slideworks/Deckary allow up to 15. Treat 5–6 as a floor for punchiness and 15 as the ceiling.
- Title must let the reader "only read the title to understand the primary message." Prefer takeaways over summaries of activity: "8 potential high-impact cost reduction levers identified" beats "We interviewed experts and key internal stakeholders…" (Slideworks)
- Titles are specific and quantified: "Optimize supply chain processes to reduce costs by 20%" beats "Supply chain processes can be optimized." Active voice. (Slideworks)
- **Horizontal logic**: read the titles in sequence and they should form the complete argument; "if someone listening to the titles without seeing a single supporting element would understand the situation, the problem, and the recommendation — your horizontal logic is sound." (Autopresent)
- **Vertical logic**: "the exhibit below the headline proves that specific claim, and nothing on the page competes with it. One idea per slide. If a page makes two points, it is two pages." (Autopresent)
- **1-3-1 test**: "One key message per slide. Three to five supporting points maximum. One clear visual." (Poesius)
- Write titles first (storyline), then build slides. (Slideworks)
- **Executive summary slide** — McKinsey: "The governing message as the slide title. Three to five bullet points, each a complete claim." BCG: "two-column management summary: the left column summarizes the situation and findings; the right column states recommendations." Bain: "results-at-the-front", "bold assertions", implementation depth. (Poesius)
- Executive summaries follow Situation–Complication–Resolution with Resolution taking **60–70%** of the content. (search snippet from Poesius/Deckary cluster; **[unverified fetch]** for the exact percentage)
- Section divider slides state the section's conclusion. (Poesius)
- **Appendix**: "The main deck should contain only what's needed to make the argument. Everything else…belongs in the appendix with clear labels and cross-references." (Poesius) "Appendix contains backup for anticipated questions." (Deckary)
- **Sources and units**: "Every chart must have measurement units and source citation" (MConsultingPrep). Source line format: "Source: Company annual reports (2022-2024); McKinsey analysis" (Deckary).
- Deckary numeric extras: 2 fonts max; 3–4 colours max; "2-4 key points that support the title"; "60 seconds or less" per slide.
- The term "action title" was coined at BCG in the 1990s (search snippet; **unverified**).

### 1.3 BLUF — Bottom Line Up Front

Sources: [AR 25-50, Army Pubs PDF](https://armypubs.army.mil/epubs/DR_pubs/DR_a/ARN42124-AR_25-50-007-WEB-13.pdf); [Matt Ström-Awn, "Bottom Line Up Front"](https://mattstromawn.com/writing/bluf/) (fetched); [Wikipedia: BLUF](https://en.wikipedia.org/wiki/BLUF_(communication)); [LegalClarity BLUF](https://legalclarity.org/bottom-line-up-front-bluf-what-it-is-and-how-to-use-it/); Kabir Sehgal, HBR 2016 ["How to Write Email with Military Precision"](https://hbr.org/2016/11/how-to-write-email-with-military-precision) (paywalled excerpt; details via [kabir.cc mirror](https://kabir.cc/how-to-write-email-with-military-precision/) and [CNBC](https://www.cnbc.com/2019/04/23/ex-us-navy-officer-how-to-write-emails-with-military-precision.html)).

- AR 25-50 (quoted via Ström-Awn): "Army writing will be concise, organized, and to the point. Two essential requirements include putting the main point at the beginning of the correspondence (bottom line up front)" and using the **active voice**.
- Air Force Handbook 33-337: "get your bottom line up front (most of the time). In nearly every communication situation, you need to state your bottom line early."
- Ström-Awn: BLUF ≠ summary. "A summary recaps the whole document; BLUF captures 'the decisive moment of your argument'" — the sentence or two that most directly reflects your point of view. Caveat: "skeptical audiences may dismiss content after a direct opening."
- BLUF vs topic sentence (LegalClarity): "This memo addresses the proposed budget revision" is a topic sentence; "I recommend we cut the Q3 marketing budget by $200,000 to cover the unexpected facilities cost" is a BLUF.
- Sehgal's email protocol: subject line starts with a keyword — **ACTION, SIGN, INFO, DECISION, REQUEST, COORD** — then BLUF in the first line, active voice ("put the noun in front of the verb"), "economy of words", and attachments/links rather than long bodies.
- Historical precedent: Churchill's "Brevity" memo, 9 Aug 1940 ([Wikiquote](https://en.wikiquote.org/wiki/Brevity); [HKS Policy Memos](https://policymemos.hks.harvard.edu/links/memo-winston-churchill-war-cabinet-re-brevity-date-08091940)): "Nearly all of them are far too long. This wastes time, while energy has to be spent in looking for the essential points." "The aim should be Reports which set out the main points in a series of short, crisp paragraphs." "Let us have an end of such phrases as these, 'It is also of importance to bear in mind the following considerations…', or 'Consideration should be given to the possibility of carrying into effect…' Most of these woolly phrases are mere padding, which can be left out altogether, or replaced by a single word." "Let us not shrink from using the short expressive phrase, even if it is conversational."

### 1.4 Amazon narrative memos (6-pager, PR/FAQ) and the "no PowerPoint" email

Sources: [CNBC 2018](https://www.cnbc.com/2018/04/23/what-jeff-bezos-learned-from-requiring-6-page-memos-at-amazon.html); [Slab – Bezos writing strategy](https://slab.com/blog/jeff-bezos-writing-management-strategy/) (fetched); [Anecdote – six-page narrative structure](https://www.anecdote.com/2018/05/amazons-six-page-narrative-structure/) (fetched); [Commoncog – Working Backwards summary](https://commoncog.com/working-backwards/); [Charter – Working Backwards briefing](https://www.charterworks.com/book-briefing-working-backwards-by-colin-bryar-and-bill-carr/); [Amazon Chronicles – Dave Limp](https://amazonchronicles.substack.com/p/working-backwards-dave-limp-on-amazons).

- Bezos email of 9 June 2004: "The reason writing a good 4 page memo is harder than 'writing' a 20 page powerpoint is because the narrative structure of a good memo forces better thought and better understanding of what's more important than what." PowerPoint lets you "gloss over ideas, flatten out any sense of relative importance, and ignore the interconnectedness of ideas." Attendees must arrive with "well structured, narrative text." (Slab; CNBC)
- Bezos (2018 shareholder letter, via CNBC): "The great memos are written and rewritten, shared with colleagues who are asked to improve the work, set aside for a couple of days, and then edited again with a fresh mind… a great memo probably should take a week or more."
- Working Backwards norms (Bryar & Carr, via Commoncog/Charter): **six pages, "no gimmicky formatting to cram more in"**; 60-minute meeting = **20 minutes silent reading + 40 minutes discussion**; every attendee must be able to read the whole thing in the 20 minutes; **Tenets** section stating the principles the recommendation rests on; appendices unlimited and data-backed; PR/FAQ variant = one-page press release + FAQ.
- Bezos on why narrative beats slides for questions (via Anecdote): "If you read the whole six-page memo, on page 2 you have a question but on page 4 that question is answered."
- Anecdote's proposed narrative skeleton: "In the past it was like this … Then something happened … So now we should do this … So the future might be like this …" with causal connectives ("But then…", "Because of that…").
- Slab's four-section template: objective; past attempts; how this approach differs; why Amazon should care.
- **Point of disagreement with the deck school**: Amazon/Tufte argue bullets fragment logic; MBB argue a disciplined deck with full-sentence titles *is* a narrative. Reconciliation used by most practitioners: prose for the decision document, deck for the meeting, appendix for evidence.

### 1.5 Gene Zelazny, *Say It With Charts*

Sources: [antoinebuteau.com/lessons-from-gene-zelazny](https://www.antoinebuteau.com/lessons-from-gene-zelazny/) (fetched); [Google Books](https://books.google.com/books/about/Say_It_With_Charts_The_Executive_s_Guide.html?id=9WnzStbbffcC).

- "The purpose of a chart is not to show data, it is to convey a message."
- "Every chart and every slide should have a clear, declarative headline that states the main message." E.g. "Industry Sales Will Double by 2025" not "Industry Sales 2020-2025."
- Five message types → five chart forms: component (pie), item (bar), time series (column/line), frequency distribution (histogram), correlation (scatter).
- "The more you can remove from a chart without losing its meaning, the better." "Avoid 3-D effects."
- "Your audience should be able to understand the message of your chart in less than 15 seconds."
- "If you can't write the message, you don't know what you're charting."

### 1.6 Nancy Duarte

Sources: [HBR 2012, "How to Present to Senior Executives"](https://hbr.org/2012/10/how-to-present-to-senior-execu) (excerpt fetched); [Duarte blog – 5 practical tips](https://www.duarte.com/blog/how-to-effectively-present-to-senior-executives/) (fetched); [Duarte – slides you deliver vs slidedoc you leave behind](https://www.duarte.com/blog/the-slides-you-deliver-versus-the-slidedoc-you-leave-behind/) (fetched); [Duarte – 5 exec-comms tips](https://www.duarte.com/blog/must-have-tips-for-executive-communications/) (fetched); [Slidedocs](https://www.duarte.com/resources/books/slidedocs/).

- "They won't sit still for a long presentation with a big reveal at the end. They'll just interrupt you before you finish."
- **Summarize up front**: "Pretend your 30-minute slot is cut to 5 minutes" — lead with findings, conclusions, recommendations, call to action.
- **Set expectations**: "the first few minutes presenting your summary and the rest of the time on discussion."
- **10% rule**: "if your appendix is 50 slides, create 5 summary slides."
- "Lead with your findings and your recommendation, tell them up front how you'll spend their meeting time, and keep the rest of your detail in an appendix." "Let the group drive the conversation, and refer to appendix slides as relevant questions and comments come up."
- Give them what they asked for, first.
- **Presented deck vs slidedoc**: "When you have different uses for your deck, you need different decks." Projected slides: cinematic, minimal text. Slidedoc: standalone, reads without a presenter. Do not produce "dense, wordy slides" to serve both — build the projected deck and generate the leave-behind from Notes View.
- Slidedoc density: one key message per slide; ~100 words per slide; **over 250 words, write a document instead** (search snippet from FlowVella/LucaPallotta summaries; **[unverified fetch]** of the exact figures).
- Exec comms tips: "it's not about what you want to say, it's about what the *audience* needs to hear"; "Avoid using jargon and technical terms"; leave "irrelevant, overly-technical details out."

### 1.7 Josh Bernoff, *Writing Without Bullshit*

Sources: [Chapter 1 PDF](https://bernoff.com/wp-content/uploads/2023/05/Writing-Without-Bullshit-Chapter-1.pdf) (extracted with pdftotext); [survey blog post](https://bernoff.com/blog/new-research-on-business-writing-infographic-and-report) (fetched); [WordRake summary](https://www.wordrake.com/blog/why-we-must-improve-business-writing).

- **Iron Imperative**: "Treat the reader's time as more valuable than your own."
- **Meaning ratio** = meaningful words / total words. "A passage with a meaning ratio of 80% is readable. But once you get below 70%, you're in bullshit territory." Worked example: 92-word mission statement cut to 54 words.
- Mentor's rule quoted approvingly: "Net it out in three clear points."
- Chapter titles give the rule list: Write Short; Front-Load Your Writing; Purge Passive Voice; Replace Jargon; Eliminate Weasel Words; Be Direct; Use Numbers Wisely; Reveal Structure; Craft Actionable Reports.
- Survey (2016, n=547 business writers): effectiveness of what they read rated **5.4/10**; **81%** agree "Poorly written material wastes my time"; top complaints: too long, poorly organized, unclear, jargon-filled, imprecise. Only 18% of writers 55+ fear "Taking a clear stand in my writing would damage my career" — Bernoff's point being that hedging is a junior habit.

### 1.8 HBR guidance (beyond Duarte and Sehgal)

- Bill Birchard, HBR Jul–Aug 2021, ["The Science of Strong Business Writing"](https://hbr.org/2021/07/the-science-of-strong-business-writing) (paywalled; features confirmed via [Bernoff's review](https://bernoff.com/blog/the-value-of-bill-birchards-eight-ss-for-strong-business-writing) and [AAPL reprint](https://www.physicianleaders.org/articles/the-science-of-strong-business-writing)): eight features that light up readers' reward circuits — **simplicity, specificity, surprise, stirring language, seductiveness, smart ideas, social content, storytelling**. Relevant to execs: specificity (a number, a name) and simplicity.
- HBR/Harvard Business Impact on boards (via [USC summary](https://communicationmgmt.usc.edu/blog/high-level-of-communication)): "Board members don't need to know the details of processes; they need to know the strategic implications, how to reduce risk, and what the business results will be." Executives "who talk too much lose credibility instead of gaining it." Executives spend ~75% of time on communication. (Secondary summary; treat as directional.)

### 1.9 Stanford GSB / Wharton

- Matt Abrahams, Stanford GSB, ["Class Takeaways — Essentials of Strategic Communication"](https://www.gsb.stanford.edu/insights/class-takeaways-essentials-strategic-communication) (fetched): the core template is **"What? So what? Now what?"** Define what you want the audience to **Know, Feel, Do**. "We start by saying, 'This is what I want to say,' rather than thinking about what our audience needs to hear." Elsewhere attributed to him: "Brevity conveys conviction" (search snippet; **unverified quote**).
- Wharton — Jonah Berger et al., ["Can Hedging Make You a Better Communicator?"](https://knowledge.wharton.upenn.edu/article/can-hedging-make-you-a-better-communicator/) (fetched) — see §2.2.

### 1.10 UK Civil Service: submissions to ministers

Sources: [civilservant.org.uk – Submissions](https://www.civilservant.org.uk/skills-submissions.html) (fetched); [Working with Ministers handbook PDF](https://www.civilservant.org.uk/library/2015_Working_with_Ministers.pdf); [Government Campus – Advising and Briefing](https://content.governmentcampus.co.uk/cross-civil-service/advising-and-briefing.pdf); [Directory of Civil Service Guidance Vol. 2](https://assets.publishing.service.gov.uk/media/64b12c4548826b00103a9e31/guide-civil-service-guidance-volume-2_0.pdf).

- Structure: **Issue → Recommendation → Timing → Background → Argument → Presentation** (handling/comms). "If the issue is a simple one, you can condense the issue, recommendation and timing into one paragraph, but the other items should always be kept separate."
- Length: "Because Ministers are under constant pressure, you should be as succinct as possible — **no more than two or three pages** of typescript." Detail goes in annexes.
- Recommendation: "If possible, you should phrase your advice so that the Minister can just say 'yes' or 'no'. **Do not merely recommend a discussion with officials.**"
- Audience model: "an intelligent non-expert who needs them to communicate with clarity and brevity." Background often reducible "to a couple of sentences."
- Options: "Summarise all the reasonably possible options and deal (perhaps briefly) with the merits and demerits of each one."
- Common mistakes: using email or PowerPoint for important decisions; recommending further discussion instead of action; ignoring the individual minister's preferences.
- GOV.UK style guidance (index page fetched; the sub-page with the 25-word sentence rule returned 404 during this session — **[unverified]** this session, but the "Use clear language" guidance historically specifies sentences under 25 words and plain-English word list).

### 1.11 Government of Canada briefing notes

Sources: [Queen's University School of Policy Studies, GovTalk 2.1 Briefing Notes: Introduction (PDF)](https://www.queensu.ca/sps/sites/spswww/files/uploaded_files/GovTalk/2_%20BN_INTRO_2021.pdf) (extracted); [Carleton – Note on Briefing Notes](https://carleton.ca/profbrouard/wp-content/uploads/noteonBriefingNotes20220901.pdf); [PPSC Deskbook ch. 48](https://www.ppsc-sppc.gc.ca/eng/pub/fpsd-sfpg/fps-sfp/fpd/ch48.html) (snippet: "Briefing notes should generally not exceed two pages" — **[unverified fetch]**); [BCcampus – Briefing Notes](https://pressbooks.bccampus.ca/missionmessagemedium/chapter/3-2-1-briefing-notes/) (403).

Queen's guide, verbatim rules:
- Standard elements: Briefing Note for / Subject-Issue / **Purpose** ("For Decision… Be time sensitive… need a decision by a certain time") / **Summary** ("Think of this as your B.L.U.F.… what you would say to the reader if that person said: 'I don't have time to read this right now. Give me your elevator version.'") / Background / Considerations / Recommendation ("The reader should already know this from the Summary.") / Speaking notes.
- "Sharp Language: Avoid verbiage and edit it down. Keep it unadorned."
- "Avoid Discursive Side Comments: Seeing something like, 'It is interesting in this regard to note the study made on this topic several years ago…' suggest this is not a briefing."
- "Write for Skimming: Avoid Long Paragraphs: Heavy texts that cover most of one page will simply not be read."
- "A briefing of one long bulleted list is not a list. Give each one a heading."
- Background is "the swamp in which many briefing notes get lost with too much detailed background that the reader probably already has."
- Options: "real options not what has been called the **Phony Three**, in which there is only one option, and the others are not viable. If no options exist, say so."
- Risk: "avoid the term 'this is a risky option' without being very specific about what it means." "Never leave a risk or impediment dangling. The user will inevitably ask, what are you doing about it?"
- "avoid being grandiose and not every issue relates to the unity of the country."
- Many users "will mandate one-pager briefs for all topics."

### 1.12 Australian public sector briefs

Sources: [Advoc8 – Writing a Ministerial Briefing Note](https://www.advoc8.co/blog/writing-a-briefing-note) (fetched); [The Mandarin – five ways to get your brief read](https://www.themandarin.com.au/2220-communications-five-ways-get-brief-read-ministers/) (paywalled); [AFP Better Practice Guide on Ministerial Briefings](https://www.afp.gov.au/sites/default/files/PDF/IPS/BPGMinisterialBriefingsforInvestigations-13012021.pdf); [Victoria ABC Common Templates Standard](https://www.vic.gov.au/sites/default/files/2019-09/ABC-Common-Templates-Standard.PDF).

- Length: "double-sided A4 page" maximum (Advoc8); "distil the 'what, who, when, where, how and why'… down to a double-sided A-4 page" (search snippet).
- "Say exactly what you want done… if you're not sure exactly what you're asking for, don't expect the Minister to be either."
- Relevance test: "why should I care?" — link to portfolio, budget, and "how does it affect voters in the seats the government needs to hold or win?"
- "Skip the PowerPoint slide pack — it adds bulk without adding clarity."
- Test with "a colleague who isn't across the issue."
- The brief "is the only thing that stays behind after a meeting."

### 1.13 Board papers (UK and Australia governance bodies)

Sources: [Good Governance Institute – Short, effective board papers](https://www.good-governance.org.uk/publications/insights/short-effective-board-papers) (fetched); [GGI – Writing board papers](https://www.good-governance.org.uk/publications/insights/writing-board-papers); [Governance Institute of Australia – Board papers guidance](https://www.governanceinstitute.com.au/advocacy/guidance-board-papers/) (403; **[unverified fetch]**, snippet: "Three to four pages of text, or 2,000 words, is about right"; "plain English"; "include a clearly delineated recommendation or resolved clause"; "offer a number of ways (three or four) to solve the problem"); [Board Intelligence – definitive guide to decision papers](https://www.boardintelligence.com/en-us/blog/the-definitive-guide-to-decision-papers) (fetched); [Board Intelligence – board pack size research](https://www.boardintelligence.com/blog/in-the-boardroom-size-matters) (fetched); [NPC – better board papers](https://www.thinknpc.org/resource-hub/how-to-create-better-board-papers/).

GGI verbatim:
- "Keep the length of papers down so they can be easily read and assimilated. **Three pages is about right.**"
- "Start with a statement of what is being asked of the directors, together with a description of who else has considered the paper and a short executive summary."
- Include "a clear and reasoned recommendation" and "an analysis of the risks of the proposal."
- "**Keep your sentences short – an average of 15 to 20 words.** Try to stick to one main idea in a sentence."
- "Choose active verbs – *we will do it* rather than *it will be done*."
- "Use everyday English… Avoid jargon and legalistic words and always explain any technical terms."
- Classify every paper: for decision, for discussion, for assurance.

Board Intelligence decision-paper framework (fetched):
- Main paper **≤ 4 pages + 1-page executive summary**; exhibits up to 20 pages, not required reading. "Two pages of words. Four is acceptable in some cases, eight is definitely too much."
- Five questions: (1) **What am I asking of you?** (visibility / input / decision) (2) What is the need or opportunity, and **why now?** (3) What do we propose to do and why? — assumptions, risks and mitigations, stakeholder impact, people to deliver, competitive context (4) **What options did we consider?** — including doing nothing (5) What do we need to do next? — steps and **resource requirements**.
- Cites McKinsey: decision "process mattered more than analysis — by a factor of six."

---

## 2. Empirical and survey evidence on what executives want

### 2.1 Reading time and attention

- **Board packs**: average board member reads the pack for "just shy of four hours", a 30% increase since 2011; "more than half now have a board pack of 200+ pages — with some pushing 1,000 pages"; "almost half of the average board pack is going unread." Directors whose packs had *not* grown reported more strategic focus (75%). n=50 (72% company secretaries), FTSE-weighted. ([Board Intelligence](https://www.boardintelligence.com/blog/in-the-boardroom-size-matters))
- **Amazon**: memo must be fully readable in 20 minutes by everyone in the room (Working Backwards, via [Commoncog](https://commoncog.com/working-backwards/)).
- **Bernoff survey** (n=547): read-material effectiveness 5.4/10; 81% say poor writing wastes their time. ([bernoff.com](https://bernoff.com/blog/new-research-on-business-writing-infographic-and-report))
- **Zelazny**: chart message grasped in <15 seconds. Deckary: ≤60 seconds per slide. Duarte: assume a 30-minute slot becomes 5.
- I found **no peer-reviewed eye-tracking or reading-time study specific to C-suite memo reading**. Claims like "executives spend 30 seconds on the first page" circulate without a traceable source; do not cite them.

### 2.2 Hedging and confidence

- **Powerless speech literature**: hedges ("sometimes", "sort of", "maybe"), hesitations, and tag questions make speakers be "evaluated as less competent, less intelligent, less attractive, less trustworthy, and less certain" (Hosman 1989 and successors). [Blankenship & Holtgraves 2005, *J. Language & Social Psychology*](https://doi.org/10.1177/0261927x04273034): under high relevance, powerless markers produced less favourable attitudes; **"strong arguments were no more persuasive than weak arguments when the message contained any of these markers."** Burrell & Koper (1998) meta-analysis of 16 studies: powerful language more persuasive and more credible. (Findings via search summaries of the abstracts; the DOI is the primary.)
- **Nuance — Berger, Oba & Boghrati (Wharton/HBS/ASU, *J. Consumer Psychology*)**, seven studies ([Knowledge at Wharton](https://knowledge.wharton.upenn.edu/article/can-hedging-make-you-a-better-communicator/), fetched): hedges differ on two axes — **likelihood** (low: "might", "could"; high: "likely", "should", "arguably") and **perspective** (general: "probably"; personal: "in my opinion", "to me"). **High-likelihood + personal-perspective hedges are most persuasive because they signal confidence.** Berger: "Hedge with the right amount of uncertainty, or call out the uncertainty" — e.g. "This could work, but we need these three things to happen first."
- **Bernoff**: fear of "taking a clear stand" is lowest among the most senior writers (18%), i.e. senior people write with less hedging.
- **Reconciliation for the profile**: ban stacked and impersonal hedges ("could potentially", "it may be the case that", "there is a possibility"); permit one owned, calibrated hedge with a condition ("I expect X; the risk is Y, and we'll know by Z").

### 2.3 Jargon and trust

- [Shulman, Dixon, Bullock & Colón Amill 2020, *J. Language & Social Psychology*](https://journals.sagepub.com/doi/10.1177/0261927X20902177), N=650: jargon reduces processing fluency **even when definitions are provided**, lowers perceived understanding and interest, and increases motivated resistance to persuasion.
- [Bullock & Bisbey 2025, *International Journal of Business Communication*](https://journals.sagepub.com/doi/10.1177/23294884251364525): "Jargon in the Workplace Reduces Processing Fluency, Self-Efficacy, and Information Seeking and Sharing" (title; abstract fetch returned 403).
- [Littrell 2026, *Personality and Individual Differences* 255:113699](https://www.sciencedirect.com/science/article/abs/pii/S0191886926000620), Cornell, 4 studies, N=1,018: the Corporate Bullshit Receptivity Scale; receptivity to phrases like "leveraging cross-functional synergies" is "negatively associated with measures of analytic thinking" and "a robust negative predictor of work-related decision-making." ([Cornell Chronicle](https://news.cornell.edu/stories/2026/03/workers-who-love-synergizing-paradigms-might-be-bad-their-jobs))
- Preply 2022 survey (1,500+ US office workers) and Kickresume 2025 (100 posts on X/LinkedIn): "circle back" and "synergy" most mocked; 85% of jargon tweets negative. ([Mental Floss](https://www.mentalfloss.com/language/slang/most-hated-office-jargon-2025), fetched)
- Multi-country survey (8,000+ professionals, 8 countries): 58% say colleagues overuse jargon; nearly half would eliminate it because deciphering "causes stress and slows down productivity." ([Fortune 2024](https://fortune.com/2024/12/24/your-gen-z-and-millennial-employees-hate-when-you-use-these-corporate-buzzwords); survey attributed to LinkedIn/Duolingo in press — **[unverified primary]**)

### 2.4 What makes executives distrust a document

- Missing "what am I asking of you" (Board Intelligence; GGI; civilservant).
- Recommending "a discussion" instead of a decision (civilservant).
- Phony options (Queen's "Phony Three").
- Unlabelled or unspecific risk ("this is a risky option") and risks left "dangling" without mitigation (Queen's).
- Background the reader already knows (Queen's; civilservant; Duarte).
- Charts without units/sources (MConsultingPrep; Deckary).
- Visible heavy AI assistance: sincerity drops from 83% to 40–52%, professionalism from 95% to 69–73% (Coman & Cardon 2025, n=1,100, [*IJBC*](https://www.sciencedaily.com/releases/2025/08/250811104226.htm), fetched).
- Powerless markers (§2.2).

---

## 3. Deck-specific mechanics

| Mechanic | Rule | Source |
|---|---|---|
| Action title | Full sentence stating the conclusion; ≤ 2 lines; ≤ 15 words; active voice; quantified where possible | Slideworks; Deckary; Poesius; Zelazny |
| Title outlier | "about 5-6 words" | MConsultingPrep (disagrees; treat as stylistic floor) |
| One idea per slide | "If a page makes two points, it is two pages" | Autopresent; Poesius 1-3-1 |
| Supporting points | 3–5 (Poesius) / 2–4 (Deckary) per slide; groupings 3–7 (Minto) | as cited |
| "So what" | Title is the so-what; body proves it (vertical logic) | Slideworks; Autopresent |
| Horizontal logic | Titles alone tell the whole story | Autopresent; Slideworks |
| Executive summary slide | First content slide; governing message as title; 3–5 complete-claim bullets (McKinsey) or two-column situation/recommendation (BCG); Resolution ≈ 60–70% of it | Poesius |
| Summary : appendix ratio | 10% rule (50 appendix → 5 summary slides) | Duarte |
| Appendix | Everything not needed for the argument; numbered and cross-referenced; used reactively in Q&A | Poesius; Deckary; Duarte |
| Time per slide | ≤ 60 seconds | Deckary |
| Chart labelling | Units and source on every chart; source line format "Source: X (years); Firm analysis"; strip gridlines/3-D; message in <15 s | MConsultingPrep; Deckary; Zelazny |
| Number formatting | Round to what the decision needs ($5.2M not $5,243,000; 14.6% not 14.62%); one unit scale across the deck | [SlideBazaar](https://slidebazaar.com/blog/the-number-formatting-rules-for-polished-financial-presentations/) (practitioner blog, low authority — corroborates common consulting practice but no firm-level source found) |
| Walls of bullets | Bullets are "pre-sentence grunts" that "can't signify logical relationships"; Columbia CAIB cited PowerPoint culture as a cause | Tufte, *Cognitive Style of PowerPoint* via [Edward Tufte notebook](https://www.edwardtufte.com/notebook/new-edition-of-the-cognitive-style-of-powerpoint/), [Eyrie review](https://www.eyrie.org/~eagle/reviews/books/0-9613921-5-0.html) |
| Speaker notes vs on-slide | Projected slide = minimal text; notes/handout carry detail; never read slides aloud; build leave-behind from Notes View | Duarte; Garr Reynolds via [Manner of Speaking](https://mannerofspeaking.org/2016/11/20/quotes-for-public-speakers-no-246-garr-reynolds/) |
| Pre-read deck (slidedoc) | ~100 words/slide, one message; >250 words → write a document | Duarte Slidedocs (figures **[unverified fetch]**) |
| 10/20/30 | 10 slides, 20 minutes, 30-pt font; rationale: "a normal human being cannot comprehend more than 10 concepts in a meeting"; 20 min leaves time for Q&A | Kawasaki via [Think Insights](https://thinkinsights.net/consulting/10-20-30-rule-presentation) (original 403) |
| 10/20/30 critique | Designed for VC pitches; Kawasaki himself said not to apply it "pedantically"; unsuitable for board plans, regulatory, keynote; Tufte and Bezos reject slide-first altogether | Think Insights; [Six Minutes](http://sixminutes.dlugan.com/flashback-friday-2/); Slab |
| Fonts/colours | ≤ 2 fonts; 3–4 colours | Deckary |

---

## 4. Tone specifics

### 4.1 Confidence calibration
- Default: declarative. Hedges "lessen the impact of strong arguments" (Blankenship & Holtgraves).
- When uncertain: **name the uncertainty and its condition** rather than soften the verb — "This could work, but we need these three things to happen first" (Berger). Prefer high-likelihood, owned hedges ("I expect", "we believe… likely") over "might/could/potentially".
- Never stack: "could potentially", "may eventually", "it is possible that it might" (this repo's SKILL.md already flags hedge stacks; extra-strict for executive).
- Announce what you don't know as a fact with a date: "We will have the Q3 number on 14 Oct" (Queen's: don't leave impediments dangling).

### 4.2 Recommendation vs options
- Always recommend. "Do not merely recommend a discussion with officials." Phrase so the reader "can just say 'yes' or 'no'." (civilservant)
- Show real alternatives considered, including "doing nothing" (Board Intelligence), but no "Phony Three" (Queen's). Governance Institute of Australia suggests three or four ways (**[unverified fetch]**).
- "Executives buy the answer, not your research. Come with a hypothesis, not an open question." ([Orvo](https://www.getorvo.com/learn/executive-communication-strategy), coach blog; corroborates but low authority)

### 4.3 Quantify the ask
- State money, people, and time explicitly (Board Intelligence Q5 "resource requirements"; Sehgal's DECISION/REQUEST subject keywords; LegalClarity's BLUF example "$200,000").
- Name the decision deadline: Queen's "need a decision by a certain time"; civilservant's separate **Timing** heading.

### 4.4 Risks and decisions needed
- Every paper opens with the type of ask (decision / discussion / assurance — GGI; visibility / input / decision — Board Intelligence).
- Risks specific, factual, with mitigation and owner (Queen's; GGI "analysis of the risks of the proposal").

### 4.5 Ownership language, voice, verbs
- Active voice mandated by AR 25-50, GGI ("we will do it rather than it will be done"), Bernoff ("Purge Passive Voice"), Sehgal.
- Own recommendations: "I recommend" / "we recommend" not "it is recommended". Passive "can be used to obscure responsibility" ([Gilliam Writers Group](https://www.gilliamwritersgroup.com/blog/writing-with-intent-using-active-and-passive-voice-strategically-in-business); [UCLA UWC handout](https://www.wp.ucla.edu/wp-content/uploads/2016/01/UWC_handouts_Active-vs-Passive-Voice-revised.pdf)).
- First person vs institutional: Amazon memos speak as "we" for the team and omit author names (Anecdote); UK submissions are written in the official's voice with "I recommend"/"we recommend"; Bernoff's rewrite gains meaning by "using words like 'we' and 'you'". No source I found endorses the impersonal institutional voice ("It is the view of the department that…") for decision documents. **Evidence here is thinner than elsewhere** — treat as a preference supported by active-voice rules rather than a proven norm.
- Verbs: concrete action verbs in titles and recommendations ("cut", "approve", "hire", "stop") rather than "leverage", "drive", "enable", "optimize" (Slideworks examples; jargon lists §5).

### 4.6 Sentence and paragraph length
- Sentences average **15–20 words**, one idea each (GGI). GOV.UK's public-content rule is ≤25 words (**[unverified this session]**).
- Paragraphs short: "Heavy texts that cover most of one page will simply not be read" (Queen's); "short, crisp paragraphs" (Churchill).
- Bernoff meaning ratio ≥ 80%.

### 4.7 Jargon
- Avoid and explain any unavoidable technical term (GGI; Duarte; Advoc8). Jargon lowers fluency even with definitions (Shulman 2020), so prefer replacement over glossing.

---

## 5. Anti-patterns

### 5.1 Reads as junior / padded / deferential
Sources: [HubSpot](https://blog.hubspot.com/service/email-phrases) (fetched), [PartnerStack](https://partnerstack.com/articles/work-email-phrases-to-stop-using-what-to-say-instead), [ZenBusiness](https://www.zenbusiness.com/blog/ten-deadliest-words/), Churchill, Bernoff, Queen's.

- Openers: "I wanted to reach out", "I hope this email finds you well", "Sorry to bother you", "Just checking in", "I just wanted to…", "I'm reaching out because…", "As per my last email", "As I mentioned before".
- Attachment/reference filler: "Please find attached", "Please note the attached", "for your perusal", "as per", "above-mentioned", "Please do not hesitate to contact me".
- Weasel/wishy-washy: "I'll try", "To be honest with you", "hopefully", "somewhat", "arguably", "it seems that".
- Churchill's padding: "It is also of importance to bear in mind the following considerations…", "Consideration should be given to the possibility of carrying into effect…".
- Discursive asides: "It is interesting in this regard to note…" (Queen's).
- Grandiosity: linking a routine issue to the national agenda (Queen's).
- Topic sentences posing as BLUF: "This memo addresses…", "The purpose of this document is to…" (LegalClarity; Ström-Awn).
- Structural: background before the ask; recommendation buried on page 3; "recommend a discussion"; options that are not real.

### 5.2 Reads as consultant-y / buzzword
Sources: Kickresume/Mental Floss; Preply; Notta via [PRSA](https://www.prsa.org/article/touching-base-on-annoying-corporate-jargon-ST-Feb25); [El Paso Inc / WSJ syndicate](https://www.elpasoinc.com/leverage-reach-out-circle-back-the-corporate-jargon-we-hate-the-most/article_e5aab474-2a97-4012-b413-616935a21843.html); Littrell 2026 item examples.

- "circle back", "synergy/synergies", "leverage" (verb), "reach out", "touch base", "low-hanging fruit", "bandwidth", "take this offline", "lean in", "agile" (as adjective for people), "new normal", "give 110 percent", "move the needle", "deep dive", "at the end of the day", "going forward", "align/alignment", "value-add", "best-in-class", "paradigm", "cross-functional synergies", "boil the ocean", "north star", "learnings", "double-click on".
- Bernoff's meaning-ratio test catches the rest: "seamless, end-to-end capability", "large proprietary datasets, advanced… sophisticated…".

### 5.3 Reads as AI-generated (LLM tells in business writing)
Sources: [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) (fetched); Coman & Cardon 2025; ZeroBounce survey via [MarketingProfs](https://www.marketingprofs.com/charts/2025/53844/how-ai-is-used-for-workplace-emails-study-zerobounce) (403; snippet: top tells are "language is too formal or robotic" 59%, "word choice feels unnatural" 50% — **[unverified fetch]**); [Liang et al. 2025, *Patterns*](https://www.cell.com/patterns/fulltext/S2666-3899(25)00214-4) (up to **24% of corporate press-release text** LLM-generated by late 2024; ~18% of consumer complaints); this repo's SKILL.md.

- Vocabulary (Wikipedia, by era): "delve", "tapestry", "testament", "underscore", "pivotal", "crucial", "landscape", "intricate", "meticulous", "vibrant", "bolstered", "garner", "interplay", "enduring" (2023–24); "align with", "fostering", "enhance", "highlighting", "showcasing", "emphasizing" (2024–25+).
- Structures: negative parallelism ("not just X, but Y"; "it's not X — it's Y"), rule-of-three lists, "It's important to note", "In today's fast-paced business environment", copula avoidance ("serves as", "stands as", "represents"), vague attribution ("industry reports", "experts argue"), "Challenges and Future Outlook" sections, em-dash clusters, bold-label inline lists, title-case headings, sycophantic openers/closers ("Great question", "I hope this helps", "Let me know if you need anything else").
- Email-specific: "I hope this message finds you well", "I wanted to follow up", "Certainly!", "Absolutely", perfectly parallel three-bullet bodies, a closing that restates the opening.
- Business consequence: heavy AI assistance in supervisor messages → sincerity 83% → 40–52% (Coman & Cardon). Employees tolerate light editing but penalise AI doing "the heavy lifting", especially for messages needing empathy or personal feedback.
- Executive-specific AI tells (synthesised from the above, not a single source): a "balanced" memo that never recommends; symmetrical pros/cons lists; risks with no owner; "stakeholders" without names; round-numbered but unsourced figures; an executive summary that summarises the *document* rather than the *decision*.

---

## 6. How existing AI-writing style guides handle executive/business tone

- **This repo (`SKILL.md` v3.12.0)** and upstream [conorbronsdon/avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing): business register is covered by the `professional` voice ("Active voice… Prefer a concrete claim per paragraph… Low tolerance for hedging") and the `blunt` voice ("Lead with the claim… Near-zero hedging… *Decision memos*, thought leadership"), plus `investor-email` ("High-trust audience. Tighten everything; promotional language is the biggest risk") and `external-email` (primary tell: face-saving pragmatic hedges, citing Navneet et al. arXiv:2602.22145 on 71.5% LLM erasure of politeness markers) context profiles. The tolerance matrix marks Hedging and Hedge-stacked predictions **extra strict** for `external-email`/`investor-email`. **Gaps**: no BLUF/answer-first structural check; no "decision requested / ask quantified / deadline / owner" checks; no deck mechanics (action titles, one-message-per-slide, appendix); no corporate-jargon table beyond generic AI vocabulary; no recommendation-vs-options rule; no sentence-length target for executive prose (the `warm` voice has 15–20 words, `casual` ≤14).
- [shaswatco/anti-ai-writing-style](https://github.com/shaswatco/anti-ai-writing-style): system prompt targeting statistically over-represented tells; no business-specific profile.
- [Every – AI style guides](https://every.to/guides/ai-style-guide): role-based instruction files (executive-assistant.md, etc.) describing "assumptions to operate under as this role" — persona, not executive-reader rules.
- Wikipedia's Signs of AI writing: explicitly descriptive, encyclopaedia-focused; no business register.
- Conclusion: **no existing skill I found encodes executive-reader conventions** (BLUF, quantified ask, decision type, options considered, risks with owners, action-title mechanics). This is new ground for the repo.

---

## 7. Where sources disagree

1. **Slides vs prose.** Bezos/Amazon and Tufte: slides fragment reasoning; write narrative. MBB and Duarte: a deck with full-sentence titles and an appendix is the executive medium. UK Civil Service: neither email nor PowerPoint for important decisions — a submission. Advoc8: "Skip the PowerPoint slide pack." Resolution: decision → prose (2–6 pages); meeting aid → deck with action titles; both → appendix.
2. **Title length.** 5–6 words (MConsultingPrep) vs ≤15 words/2 lines (Slideworks, Deckary). Use 15/2 lines as the hard cap; flag titles under ~6 words only if they've collapsed into labels.
3. **Hedging.** Powerless-speech literature: hedges always cost credibility. Berger et al.: first-person high-likelihood hedges *increase* persuasion. Bernoff: cut weasel words. Resolution: forbid impersonal/low-likelihood/stacked hedges; allow one owned, conditioned hedge.
4. **Bullets.** Tufte and Amazon: avoid. GGI and Queen's: use bullets and lists, "but well and in context… Give each one a heading." MBB: 3–5 complete-claim bullets on the exec summary. Resolution: bullets must be full claims with a heading, never bare noun phrases (already a SKILL.md rule).
5. **Options.** civilservant: options with merits/demerits; GIA: three or four; Queen's: only *real* options, and "if no options exist, say so." Board Intelligence: always include "doing nothing." Resolution: recommend one; list the real alternatives considered including no-action; never pad to three.
6. **10/20/30.** Kawasaki's heuristic is VC-specific and he disclaims pedantic application; board and regulatory decks routinely exceed 10 slides with appendices. Use "10 summary slides max before appendix" as the executive-deck form of the rule.
7. **Length.** 1 page (Queen's "many will mandate one-pagers"; Advoc8 double-sided A4) vs 2–3 pages (civilservant) vs 3 pages (GGI) vs 4 + 1 (Board Intelligence) vs 6 (Amazon). These are different genres: brief/submission ≤2–3; board decision paper ≤4+1; strategy narrative ≤6 with 20-min read test.

---

## 8. Candidate rules

### 8(a) `executive` voice profile (prose: memos, emails, briefs, board papers)

Structural
1. **BLUF in the first sentence or two**: the decision, recommendation, or key finding — not the topic. Test: could the reader stop after paragraph one and act? *(AR 25-50; Ström-Awn; Minto; Duarte; Queen's; LegalClarity)*
2. **State the ask type up front**: for decision / for discussion / for information (or visibility / input / decision). *(GGI; Board Intelligence; Sehgal ACTION/DECISION/INFO/REQUEST)*
3. **Quantify the ask**: money, headcount, time, and the decision deadline in the opening block. *(Board Intelligence Q5; civilservant "Timing"; Queen's "need a decision by")*
4. **Recommend, don't list**: one recommendation phrased for yes/no; never "recommend further discussion." *(civilservant; Board Intelligence; Orvo)*
5. **Real options only**: name alternatives considered including "do nothing"; no Phony Three; if there are no options, say so. *(Queen's; Board Intelligence; GIA)*
6. **Risks are specific, owned, and mitigated**: no "this is risky"; every risk names impact, likelihood, mitigation, and owner. *(Queen's; GGI)*
7. **Background after the answer, and short**: assume an intelligent non-expert who knows the story; background often "a couple of sentences." *(civilservant; Queen's; Minto SCQA "Situation" = agreed facts)*
8. **Length caps by genre**: email ≤ 1 screen; brief/submission ≤ 2–3 pages; board decision paper ≤ 4 pages + 1-page summary; narrative ≤ 6 pages readable in 20 minutes; detail to annex/appendix. *(civilservant; GGI; Board Intelligence; Working Backwards; Advoc8)*
9. **Pyramid the body**: 2–4 supporting arguments of the same kind, each a full-sentence heading; evidence below. *(Minto)*
10. **Subject lines carry the ask**: keyword + BLUF ("DECISION: approve £1.2m vendor contract by Fri"). *(Sehgal)*

Sentence and word level
11. **Average 15–20 words per sentence, one idea each**; short paragraphs (≤ 4 sentences); no page-length paragraphs. *(GGI; Churchill; Queen's)*
12. **Active voice; owned verbs**: "We recommend", "I will", "Finance approved" — never "it is recommended", "it was decided". *(AR 25-50; GGI; Bernoff; Sehgal)*
13. **One calibrated hedge maximum per claim, first-person and conditioned**: "I expect X; it depends on Y" — never stacked or impersonal ("could potentially", "it may be the case that", "there is a possibility"). *(Blankenship & Holtgraves; Berger et al.; Bernoff)*
14. **Numbers over adjectives**: replace "significant", "substantial", "material" with the figure; round to decision precision ($5.2M, 15%); one unit scale per document. *(Birchard specificity; Slideworks examples; SlideBazaar)*
15. **Meaning ratio ≥ 80%**: cut words that carry no information. *(Bernoff)*
16. **Corporate-jargon table (flag, replace)**: circle back → follow up on [date]; synergy → [the specific saving]; leverage (v.) → use; reach out → call/email; touch base → meet; bandwidth → time/people; low-hanging fruit → [the easy item]; take offline → discuss after; deep dive → analysis; at the end of the day → cut; going forward → from [date] / cut; align → agree; learnings → lessons; move the needle → [the metric change]. *(Kickresume/Mental Floss; Preply; PRSA/Notta; Littrell; Fortune)*
17. **Deference/padding table (cut)**: "I wanted to reach out", "I hope this finds you well", "just checking in", "sorry to bother you", "please find attached" (→ "Attached: X"), "as per", "please do not hesitate", "for your perusal", "as I mentioned before", "to be honest", "I'll try", "it is important to bear in mind", "consideration should be given to". *(HubSpot; PartnerStack; Churchill; Queen's; Bernoff)*
18. **No topic-sentence openers**: "This memo addresses…", "The purpose of this document is…". *(LegalClarity; Ström-Awn)*
19. **No discursive asides or grandiosity**: "It is interesting to note…", linkage to grand agendas. *(Queen's)*
20. **Explain or replace every technical term**; prefer replacement — definitions don't restore fluency. *(GGI; Shulman 2020)*
21. **LLM tells at extra-strict**: delve/testament/underscore/pivotal/landscape/tapestry; "it's important to note"; negative parallelism; rule-of-three padding; em-dash clusters; symmetric pros/cons that never conclude; "stakeholders" with no names; sycophantic openers/closers. *(Wikipedia Signs; Coman & Cardon; this repo's P0/P1 lists)*
22. **Never invent**: no fabricated figures, owners, deadlines, or options to satisfy rules 3–6 — flag the gap instead. *(this repo's Never-inject guardrail; Wikipedia hallucinated-citation tell)*

### 8(b) `executive-deck` context profile (slides, headlines, bullets, speaker notes)

1. **Every slide title is an action title**: a full sentence stating the conclusion; ≤ 2 lines, ≤ 15 words; active voice; quantified where the data allows. Flag label titles ("Market overview", "Q3 results"). *(Slideworks; Deckary; Poesius; Zelazny)*
2. **Horizontal-logic test**: titles read in sequence must tell the whole argument (situation → complication → recommendation). Flag a deck whose titles don't. *(Autopresent; Slideworks; Minto)*
3. **Vertical-logic test**: everything on the slide supports its title; one message per slide; "if a page makes two points, it is two pages." *(Autopresent; Poesius 1-3-1)*
4. **Executive summary is slide 1 (after title)**: governing recommendation as its title; 3–5 bullets, each a complete claim (or two-column situation | recommendation); the ask and decision deadline appear here. *(Poesius; Duarte; Board Intelligence)*
5. **10% rule and appendix discipline**: ≤ ~10 summary slides before the appendix; everything else in a numbered, cross-referenced appendix used reactively for questions. *(Duarte; Poesius; Deckary; Kawasaki as heuristic)*
6. **Bullets are claims, not noun phrases**: 3–5 per slide max, each a full sentence with a verb; no nested bullet trees. *(Poesius; Deckary; Tufte; GGI; this repo's bare-noun-phrase rule)*
7. **Speaker notes carry the narrative, slides carry the point**: on-slide text minimal in a presented deck; if the deck is a pre-read (slidedoc), one message and ~100 words per slide; >250 words means it should be a memo. *(Duarte; Reynolds)*
8. **Every chart has a message title, units, and a source line**; strip gridlines, 3-D, legends the title makes redundant; message legible in <15 s. *(Zelazny; MConsultingPrep; Deckary)*
9. **Number formatting**: consistent unit scale across the deck; 2–3 significant figures; percentages to one decimal at most unless the decision hinges on more. *(SlideBazaar — practitioner; corroborates Zelazny's simplicity rule)*
10. **"So what" check**: for each slide ask what the executive should decide or believe differently; if nothing, move it to the appendix. *(Abrahams What/So what/Now what; Slideworks)*
11. **Close with the decision slide**: the ask restated, options considered, recommendation, resources, owners, dates, next steps. *(Board Intelligence Q1–Q5; civilservant)*
12. **Tolerance-matrix settings**: Hedging **extra strict**; Hedge-stacked predictions **extra strict**; Excessive bullets **relaxed** (bullets are the medium) but Bullet lists of bare noun phrases **strict**; Title-case headings **skip** (deck convention); Em-dash overuse **strict**; Rule-of-three padding **strict**; Significance inflation **extra strict** (a "pivotal" without a number is a P0 on a deck); Colon-into-a-triple **strict**.
13. **Anti-patterns to flag**: label titles; "Agenda" slides longer than one; walls of ≥ 7 bullets; a slide with two charts and two messages; charts with no source; "Key Takeaways" slides that repeat titles verbatim; "Questions?" as the last slide instead of the decision slide; speaker notes that are the slide text pasted again. *(Tufte; Duarte; Poesius; Deckary)*

### 8(c) Auto-detection cues (for the skill's cue table)

| Cue | Profile |
|---|---|
| Headings such as "Recommendation", "Decision required", "Ask", "Options considered", "Risks", "Timing", "Resources"; salutation to a named executive/minister/board; "for decision/for noting" | `executive` voice |
| Slide-like structure: numbered slides, "Slide N", short titled blocks with 3–5 bullets, "Appendix", "Source:" lines, "Speaker notes:" | `executive-deck` context |

---

## 9. Source list (distinct sources, with what each contributed)

1. Minto via Buteau — pyramid rules, SCQA, 3–7 points. https://www.antoinebuteau.com/lessons-from-barbara-minto/
2. barbaraminto.com — provenance. https://www.barbaraminto.com/
3. Slideworks — action titles ≤15 words/2 lines, examples. https://slideworks.io/resources/how-to-write-action-titles-like-mckinsey
4. Poesius — MBB exec summary, 1-3-1, appendix. https://poesius.com/blog/how-mckinsey-bcg-bain-structure-final-presentations
5. Deckary — 15 words, 2 lines, 60 s/slide, source line. https://deckary.com/blog/consulting-slide-standards
6. MConsultingPrep — 5–6 word titles (outlier), units/sources. https://mconsultingprep.com/how-consultants-make-mbb-slides
7. Autopresent — horizontal/vertical logic quotes. https://www.autopresent.ing/blog/mckinsey-deck/
8. AR 25-50 — BLUF and active voice. https://armypubs.army.mil/epubs/DR_pubs/DR_a/ARN42124-AR_25-50-007-WEB-13.pdf
9. Ström-Awn — BLUF vs summary, AFH 33-337, Churchill. https://mattstromawn.com/writing/bluf/
10. LegalClarity — BLUF vs topic sentence. https://legalclarity.org/bottom-line-up-front-bluf-what-it-is-and-how-to-use-it/
11. Sehgal, HBR 2016 / kabir.cc — subject keywords, BLUF, active voice. https://hbr.org/2016/11/how-to-write-email-with-military-precision ; https://kabir.cc/how-to-write-email-with-military-precision/
12. Churchill "Brevity" — Wikiquote / HKS. https://en.wikiquote.org/wiki/Brevity ; https://policymemos.hks.harvard.edu/links/memo-winston-churchill-war-cabinet-re-brevity-date-08091940
13. CNBC 2018 — Bezos quotes. https://www.cnbc.com/2018/04/23/what-jeff-bezos-learned-from-requiring-6-page-memos-at-amazon.html
14. Slab — 2004 email, template. https://slab.com/blog/jeff-bezos-writing-management-strategy/
15. Anecdote — narrative skeleton, page-2/page-4 quote. https://www.anecdote.com/2018/05/amazons-six-page-narrative-structure/
16. Commoncog / Charter — Working Backwards: 6 pages, 20+40 minutes, tenets. https://commoncog.com/working-backwards/ ; https://www.charterworks.com/book-briefing-working-backwards-by-colin-bryar-and-bill-carr/
17. Zelazny via Buteau — message titles, 5 chart types, 15 s. https://www.antoinebuteau.com/lessons-from-gene-zelazny/
18. Duarte HBR 2012 — interruptions. https://hbr.org/2012/10/how-to-present-to-senior-execu
19. Duarte blog — 5-minute test, 10% rule, appendix. https://www.duarte.com/blog/how-to-effectively-present-to-senior-executives/
20. Duarte — slides vs slidedoc. https://www.duarte.com/blog/the-slides-you-deliver-versus-the-slidedoc-you-leave-behind/
21. Duarte — exec comms tips. https://www.duarte.com/blog/must-have-tips-for-executive-communications/
22. Bernoff ch.1 PDF — Iron Imperative, meaning ratio. https://bernoff.com/wp-content/uploads/2023/05/Writing-Without-Bullshit-Chapter-1.pdf
23. Bernoff survey 2016 — n=547, 5.4/10, 81%. https://bernoff.com/blog/new-research-on-business-writing-infographic-and-report
24. Birchard HBR 2021 / Bernoff review — eight S's. https://hbr.org/2021/07/the-science-of-strong-business-writing ; https://bernoff.com/blog/the-value-of-bill-birchards-eight-ss-for-strong-business-writing
25. Stanford GSB Abrahams — What/So what/Now what; Know/Feel/Do. https://www.gsb.stanford.edu/insights/class-takeaways-essentials-strategic-communication
26. Knowledge at Wharton (Berger, Oba, Boghrati) — hedge types. https://knowledge.wharton.upenn.edu/article/can-hedging-make-you-a-better-communicator/
27. Blankenship & Holtgraves 2005 — powerless markers neutralise strong arguments. https://doi.org/10.1177/0261927x04273034
28. civilservant.org.uk — submissions structure, 2–3 pages, yes/no. https://www.civilservant.org.uk/skills-submissions.html
29. Queen's SPS GovTalk — Canadian BN structure, BLUF summary, Phony Three, risk. https://www.queensu.ca/sps/sites/spswww/files/uploaded_files/GovTalk/2_%20BN_INTRO_2021.pdf
30. Advoc8 — Australian brief, double-sided A4, no slide pack. https://www.advoc8.co/blog/writing-a-briefing-note
31. Good Governance Institute — 3 pages, 15–20 words, active verbs. https://www.good-governance.org.uk/publications/insights/short-effective-board-papers
32. Board Intelligence — decision paper 4+1, five questions. https://www.boardintelligence.com/en-us/blog/the-definitive-guide-to-decision-papers
33. Board Intelligence — board pack research (4 h, 200+ pages, half unread). https://www.boardintelligence.com/blog/in-the-boardroom-size-matters
34. Governance Institute of Australia — 3–4 pages/2,000 words [unverified fetch]. https://www.governanceinstitute.com.au/advocacy/guidance-board-papers/
35. Tufte — bullets, Columbia. https://www.edwardtufte.com/notebook/new-edition-of-the-cognitive-style-of-powerpoint/ ; https://www.eyrie.org/~eagle/reviews/books/0-9613921-5-0.html
36. Kawasaki via Think Insights — 10/20/30 and caveats. https://thinkinsights.net/consulting/10-20-30-rule-presentation ; https://guykawasaki.com/the_102030_rule/ (403)
37. Mental Floss / Kickresume / Preply — jargon rankings. https://www.mentalfloss.com/language/slang/most-hated-office-jargon-2025
38. Littrell 2026, Cornell — CBSR. https://www.sciencedirect.com/science/article/abs/pii/S0191886926000620 ; https://news.cornell.edu/stories/2026/03/workers-who-love-synergizing-paradigms-might-be-bad-their-jobs
39. Shulman et al. 2020 — jargon and fluency. https://journals.sagepub.com/doi/10.1177/0261927X20902177
40. Bullock & Bisbey 2025 — workplace jargon. https://journals.sagepub.com/doi/10.1177/23294884251364525
41. HubSpot — email phrases to stop. https://blog.hubspot.com/service/email-phrases
42. Wikipedia: Signs of AI writing — LLM vocabulary and structures. https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing
43. Coman & Cardon 2025, IJBC via ScienceDaily — AI emails and trust. https://www.sciencedaily.com/releases/2025/08/250811104226.htm
44. Liang et al. 2025, Patterns — 24% of press releases LLM-assisted. https://www.cell.com/patterns/fulltext/S2666-3899(25)00214-4
45. ZeroBounce via MarketingProfs — 59%/50% detection cues [unverified fetch]. https://www.marketingprofs.com/charts/2025/53844/how-ai-is-used-for-workplace-emails-study-zerobounce
46. conorbronsdon/avoid-ai-writing and local SKILL.md — existing profiles. https://github.com/conorbronsdon/avoid-ai-writing/blob/main/SKILL.md
47. shaswatco/anti-ai-writing-style; Every AI style guide — other guides. https://github.com/shaswatco/anti-ai-writing-style ; https://every.to/guides/ai-style-guide
48. SlideBazaar — number formatting (practitioner, low authority). https://slidebazaar.com/blog/the-number-formatting-rules-for-polished-financial-presentations/
49. Fortune 2024 — 8,000-person jargon survey (primary unverified). https://fortune.com/2024/12/24/your-gen-z-and-millennial-employees-hate-when-you-use-these-corporate-buzzwords

Not found / could not verify: a peer-reviewed study of C-suite memo reading time; a first-party BCG or Bain style guide (all MBB conventions above come from ex-consultant training sites); the GOV.UK 25-word rule page (404 this session); Kawasaki's original post (403); GIA's PDF (403); The Mandarin's five tips (paywall).
