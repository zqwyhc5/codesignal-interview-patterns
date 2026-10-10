# CodeSignal interview questions: what the 70-minute GCA actually asks, real company examples, and how to prep by pattern

Getting a CodeSignal link in your inbox raises three questions at once: what's on the screen, how long you have, and which question is going to eat your clock. The platform's own name tells you nothing useful, and most prep advice online is written by people describing the old version of the test.

Here's what the assessment actually looks like now, what kinds of CodeSignal interview questions show up, and where the points that separate a 450 from a 580 actually live.

## The format is fixed, and the clock is the real opponent

The standard CodeSignal General Coding Assessment (GCA) is four coding questions in 70 minutes, all visible from the start, and you can answer them in any order. Everything is auto-graded against hidden tests.

The part most people miss: CodeSignal's published averages per question run roughly 10, 15, 20, and 30 minutes. Add that up and you get 75 minutes of intended work inside a 70-minute window. The test isn't designed for you to finish everything cleanly. It's designed to force prioritization, and the scoring reflects that.

Scores run from 200 to 600. That scale replaced the old 300–850 "Coding Score" in spring 2023, so any guide quoting 750 or 850 targets is describing a retired system. If you find a screenshot of someone's 800 from 2022, it tells you nothing about what a recruiter sees today.

One more thing worth knowing before you rehearse anything: not every CodeSignal invitation is a GCA. Companies configure their own assessments, and the invite is the source of truth for question count, duration, and whether you'll see a score at all.

## Three scoring rules that change how you should answer

**Partial credit is real.** Since spring 2023, a brute-force solution that passes some test cases earns points. A blank answer earns nothing. If Q4 stalls on you, shipping an O(n²) version that clears the smaller inputs beats spending twelve more minutes chasing an optimal solution you never submit.

**CodeSignal keeps your highest submission, not your last one.** This is documented behavior, and it's genuinely counterintuitive. If you had a passing solution on Q3, then rewrote it and introduced a syntax error, the earlier passing version is still what gets graded. The panic move of "let me just fix one more thing" only hurts you if you never banked a green run in the first place.

**The editor does not autosave between questions.** This is the quiet one. You can move between tasks freely, but code only persists if you hit Submit before leaving. People lose a working Q2 because they tabbed over to peek at Q4, changed a loop, and came back to a stale editor. Submit is free and unlimited. Use it before you touch another tab.

Also worth planning around: retakes are capped at two per rolling 30 days and three per rolling six months. A casual practice run with a real invitation attached isn't free.

## What each question slot usually contains

| Slot | Typical topics | Community-reported target time |
| --- | --- | --- |
| Q1 | Array manipulation, basic string processing, simple math, pattern printing | 5–8 minutes |
| Q2 | Hash maps, frequency counting, two pointers, sliding window, simulation | 8–15 minutes |
| Q3 | Trees, BFS/DFS on grids, 1D dynamic programming, stacks and queues, matrix work | 15–25 minutes |
| Q4 | Graph algorithms, advanced DP, interval scheduling, complex edge cases | 20–40 minutes if you attempt it |

That ordering comes from community-compiled problem sets rather than an official syllabus, so treat it as a strong tendency rather than a guarantee. Occasionally Q4 has a simpler structure than Q3, and candidates who scan all four prompts before committing tend to catch that and reorder.

The practical takeaway: Q1 and Q2 need to be automatic. If you're spending fifteen minutes on the warm-up question, no amount of Q4 skill saves the run.

## Real CodeSignal questions candidates report, by company

Community threads are the closest thing to a real question bank, and they're worth reading for shape rather than memorization. CodeSignal rotates problems, so the specific prompts below won't recur verbatim — but the difficulty curve and the topic mix do.

**Visa** (reported on LeetCode discussion threads): a prefix-sum index problem where you return the first index whose cumulative score reaches a target, a bus-schedule query that converts `HH:MM` timestamps to minutes and returns the most recent departure before a given time, a newspaper-style text justification task with width padding, and an unordered-edge island sequencing problem that reduces to topological ordering on a graph.

**ZipRecruiter**: valid parentheses with `*` wildcards (solved with a low/high range of open-bracket counts), a Meeting Rooms II variant, Task Scheduler with a cooldown, and maximum profit in job scheduling — DP combined with binary search for the last non-conflicting job.

**Pinterest**: a bipartite graph distance problem between boards and pins, an eight-direction robot vacuum grid traversal, and a variant where two vacuums cooperate.

**SIG**: one CodeSignal round asked candidates to take a naive O(N) movie-search function reading from a CSV and optimize it in 30 minutes using hashmap indexing on genre and year range. Their phone screen moved to a trie-based autocomplete problem and an OOP cash-register design.

**HubSpot behaves differently.** Candidate reports from 2025 and 2026 describe 90 minutes and four progressive levels built on a single codebase, with helper files rather than one isolated function. That's not the GCA. Assuming the standard four-question shape for a progressive build is one of the more expensive mistakes you can make on test day.

If your assessment is vocabulary-heavy rather than algorithmic — ML role variants start with multiple-choice on confusion matrices and regularization, then move to hand-computed forward passes — the four-slot model doesn't apply either.

## Certified GCA versus a custom company assessment

These are different products with the same logo, and mixing them up wastes prep time.

**Certified GCA:** four questions, 70-minute default, published modules, a 200–600 Assessment Score, and a result you can share with multiple employers if your sharing settings allow it. Setup happens before the timer starts — face photo, then photo ID, then a rules checklist.

**Custom assessment:** company-authored problems, potentially a different count and duration, role-specific formats (database, frontend, file-system), employer-assigned point values, and often no visible score to you at all. If your results page shows nothing numeric, that's usually why — and the GCA score charts floating around Reddit won't help you interpret it.

On the certified GCA, the rules are narrower than most blog posts suggest. Syntax documentation is permitted; you can look up which methods a C++ queue supports. A tutorial explaining how to implement a deque is not, because that page is doing the algorithmic thinking for you. AI tools are out — including as a disguised syntax lookup.

CodeSignal also sells a separate AI-assisted assessment built around its Cosmo co-pilot. If a company sends you that, you're taking a different test: the full interaction transcript goes to the employer, so how you ask questions becomes part of your evaluation. Targeted questions about complexity tradeoffs or missing edge cases read well. "Solve this problem for me" doesn't.

Integrity signals are worth respecting for their own sake. CodeSignal's Suspicion Score folds in paste events, telemetry patterns, and code similarity against the platform and the web. Proctoring data is reviewed by CodeSignal and isn't handed to the requesting company, but a flag can still end an application.

## What to study for CodeSignal questions specifically

Generic interview prep is a poor match for this test. The GCA rewards execution speed on problems you already recognize, not your ability to crack a novel hard problem in forty minutes. That inverts the usual advice about grinding randomly hard problems.

Three things move the score most:

**Step one: pick one language and stay in it.** You'll be writing in a browser IDE with syntax highlighting, autocomplete, and error underlining — no external editor on the certified GCA. Spend an hour in a browser-based environment before the real thing so you're not hunting for keyboard shortcuts under a timer.

**Step two: learn patterns as units, not problems as instances.** Every slot in the test maps to a small set of reusable templates: two pointers, sliding window, monotonic stack, BFS/DFS on grids, binary search on the answer, 1D DP transitions, interval scheduling. When you recognize the pattern in the first ninety seconds, you write the template and spend your remaining time on edge cases instead of on approach.

**Step three: run full 70-minute simulations.** Untimed drilling builds understanding. Timed simulation builds the pace that the test actually grades. Track where you lost minutes and label each delay specifically — "I missed the DP state definition" gives you something to fix, "dynamic programming" doesn't.

If you want a structured version of steps two and three, 👉 [AlgoMonster's pattern-based curriculum](https://algo.monster?fpr=li69) is built around exactly this split. Instead of a 3,000-problem bank, it organizes material by coding pattern with code templates, decision flowcharts for "which pattern does this problem want," and guided step-by-step walkthroughs on a curated practice set. There's also a Speedrun mode for timed review, unlimited AI assistant usage, and content covering data structures, algorithms, and low-level design.

The honest caveat: it's text-and-diagram based, entirely without video walkthroughs. If you learn better from watching someone code, this format won't click for you. And at roughly 500+ lessons and 3,000+ editorials, it's a bigger surface than the four GCA slots demand — you're buying pattern fluency for later interviews too, not just this one screen.

## AlgoMonster plans and current pricing

CodeSignal prep is the immediate use case, but the plan math matters if you'll interview again in two years.

| Plan | What you get | Price | Billing | Purchase |
| --- | --- | --- | --- | --- |
| Free | Limited access to a subset of patterns and problems — enough to judge whether the teaching style fits | $0 | No card needed | [Start on the free tier](https://algo.monster?fpr=li69) |
| Pro – Yearly | All patterns, lessons and problems; unlimited AI Assistant; unlimited Speedrun; 500+ lessons across 6 courses; 1,000+ illustrations; 3,000+ editorials; real questions from top tech companies, updated monthly | $99/year (shown as $8.25/month billed annually, about $0.28/day) | Billed annually, cancel or upgrade anytime | [Get Pro Yearly](https://algo.monster/subscribe?fpr=li69) |
| Pro – Lifetime | Everything in the annual plan plus permanent access and lifetime updates | $189 | One-time payment | [Get Pro Lifetime](https://algo.monster/subscribe?fpr=li69) |

Both paid tiers include the Foundation Course and the Build an LLM Course at no extra cost. Specialized partner courses, such as Quant Interview Prep, are sold separately. There's no monthly plan and no team or enterprise tier — it's built for individual candidates.

Pricing on the site moves with promotions, so the number you see at checkout is the one that counts. Two years of the annual plan costs more than the lifetime buy, which is the whole argument for the one-time option if you expect to job-search more than once. If you're prepping for a single interview loop in the next month, the annual plan is the lower-risk spend.

## A prep sequence that fits how the test is graded

1. Read the structure and rules documentation for your specific invitation before anything else. It takes ten minutes and it's the difference between rehearsing the right test and the wrong one.
2. Take one timed practice session without pausing to establish your baseline. Four problems, 70 minutes, one shared budget. Record where the time went.
3. Drill your weakest pattern from step two for two or three days — not a random assortment of hard problems.
4. Run a second full simulation in the language and physical setup you'll actually use: same browser, same desk, notifications off, nothing else open.
5. In the last two days, write edge cases before submitting every practice solution. Empty input, single element, duplicates, maximum size. It's the cheapest score recovery available.
6. On test day, scan all four prompts in the first three minutes. Secure Q1 and Q2 completely before touching anything else. Submit before switching tasks, always.

The candidates who do well on this test aren't the ones who solve the hardest question. They're the ones who never lose a bankable question to the clock. That's a scheduling skill more than a talent, which is good news — it's trainable in a week, and 👉 [AlgoMonster's timed practice sets](https://algo.monster?fpr=li69) give you somewhere structured to do it.
