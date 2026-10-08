[![skills.sh](https://skills.sh/b/instax-dutta/darpa-audit)](https://skills.sh/instax-dutta/darpa-audit)

# darpa-audit

Stop getting "great idea, looks solid!" from generic AI. Get a DARPA-grade verdict instead.

George Heilmeier ran DARPA and made every proposal answer eight questions before it got a cent. Most ideas do not survive number four. **darpa-audit** enforces that exact gate on your startup or project idea with 5 prompts run in order - and kills weak ideas plainly instead of helping you build them.

If you are an agent: invoke this when the user says `audit my idea`, `is this a good idea`, `should I build this`, `validate my idea`, `kill my idea`, or pastes a startup concept with no validation.

## Why darpa-audit?

Vague AI praise tells you your idea is "compelling" and misses that it needs the words "AI-powered platform" to sound interesting, that a spreadsheet already solves it well enough, and that "busy families" is not a person.

A human advisor takes days and real money to tell you the same thing.

darpa-audit gives your agent a deterministic 8-question framework: jargon strip, status quo audit, who-cares test, failure list, and week-4 / week-12 exams - with a hard SURVIVES / DOES NOT SURVIVE verdict every time.

## Install

```bash
npx skills add instax-dutta/darpa-audit --skill darpa-audit
```

Or install globally for all agents:

```bash
npx skills add instax-dutta/darpa-audit --skill darpa-audit -g -a "*"
```

Supports Claude Code, Cursor, Codex, Copilot, Windsurf, Gemini, OpenCode, Kilo Code, Codebuff, and 20+ agents via [skills.sh](https://skills.sh).

## How an agent uses it

- `audit this idea` - Full 5-prompt run, PASS/FAIL per prompt, SURVIVES / DOES NOT SURVIVE verdict
- `is this worth building` - Same gate, one revival condition if killed
- `who cares test` - Jump straight to Prompt 3, the one that does the most damage

Just drop in your idea text, pitch, or proposal. The agent runs the prompts in order and stops at the first failure - that failure IS the audit result. No extra prompting needed.

## The 8 Questions (Heilmeier Catechism, DARPA 1975)

| # | Question | Prompt that forces it |
|---|----------|----------------------|
| 01 | What are you trying to do? No jargon. | The jargon strip |
| 02 | How is it done today, and what are the limits? | The status quo audit |
| 03 | What is new in your approach, and why will it work? | The who cares test (part 1) |
| 04 | Who cares? What difference does success make? | The who cares test (part 2) |
| 05 | What are the risks? | The failure list |
| 06 | What will it cost? | The failure list |
| 07 | How long will it take? | The failure list |
| 08 | What are the midterm and final exams for success? | The exams (week 4 / week 12) |

**Run them in order.** Prompt 1 first, always - it decides whether the rest is worth running. Stop at the first one you cannot answer.

## The 5 Prompts

1. **The jargon strip** - explain it so a smart twelve-year-old follows. If it needs "AI-powered" to sound interesting, that is the finding.
2. **The status quo audit** - how is it solved today, what is specifically bad? Most app ideas die here, against a spreadsheet that already works.
3. **The who cares test** - name the specific person and what they do on a real Tuesday. "Busy families" is not a person.
4. **The failure list** - everything that has to go right, ranked by likelihood of going wrong. The ranking matters more than the list.
5. **The exams** - one measurable result at week 4, one at week 12, both failable. A number you cannot miss is not a test.

## Operating rules (held across the whole audit)

- Judge whether the idea should exist, not how to build it. No plans, architectures, or feature lists unless explicitly asked.
- Reject jargon. Never accept a market segment for "who cares".
- Label every claim [ASSUMPTION] vs [KNOWN].
- If the idea is weak, say so plainly. If it does not survive, say so.

## Proof

No hype. What you get is verifiable in [SKILL.md](skills/darpa-audit/SKILL.md): the original 8 Heilmeier questions, 5 forcing prompts with fail conditions, a PASS/FAIL-per-prompt output contract, and a SURVIVES / DOES NOT SURVIVE verdict with one revival condition. Run it on any idea and count the checks yourself.

Pairs with [market-validator](https://github.com/instax-dutta/market-validator) for a kill-then-validate flow - darpa-audit kills weak ideas fast, market-validator checks survivors against real user complaints.

If it saved you from building the wrong thing, star it.

## License

MIT

## More agent skills by me

- [flash-compare](https://github.com/instax-dutta/flash-compare) - Flash-style top-1% product comparisons, exactly how flash.co works
- [master-pitcher](https://github.com/instax-dutta/master-pitcher) - Audit, draft, or roast pitch decks with an 18-check VC framework
- [brand-vibes](https://github.com/instax-dutta/brand-vibes) - Apply any company's design language while vibecoding, 66 brand profiles
- [roadmap-tutor](https://github.com/instax-dutta/roadmap-tutor) - Learn any roadmap.sh roadmap one topic at a time, tracked across sessions
- [market-validator](https://github.com/instax-dutta/market-validator) - Validate SaaS ideas with real user complaints across 10+ platforms
- [scroll-3d-world](https://github.com/instax-dutta/scroll-3d-world) - Scroll-scrubbed 3D fly-through landing pages in Three.js, no AI video
- [google-code-review](https://github.com/instax-dutta/google-code-review) - Google's code review best practices as an agent skill
- [finetune-llm](https://github.com/instax-dutta/finetune-llm) - Hardware-aware LLM fine-tuning: probe the GPU, pick the engine, verify the result
