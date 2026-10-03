# Panel Test: UI research

Overnight research on what makes a mobile UI feel premium and calm: how the brain and eye process screens, why people like certain looks, how displays behave, and how flowing motion should work and where it should stop. Done for the PANOPTES globe app by **Paarth Jawalkar**.

Read the full write-up: [report_public_ui.md](report_public_ui.md)

## What Panel Test is
A small multi-AI research setup. Each topic gets its own chat, and each tool keeps a project called "Panel Test".

## Method
1. The same prompt per topic was sent to ChatGPT, Perplexity, DeepSeek, Gemini Pro, Claude (via arena.ai), Kimi and Grok.
2. Answers were compared head to head. Where tools disagreed, the claim was checked against a primary source (paper, Apple/W3C/MDN docs, library source code).
3. Everything was done on free tiers (ChatGPT on its low-cost plan). No monetization.

## Verified vs unverified
A number is marked **verified** only if a primary or authoritative page was opened. "An AI said it" alone is marked **UNVERIFIED**.

## The 8 contradictions
The report lists each with a verdict and sources: cone count, spring defaults, Display P3 vs sRGB size, what "1 second" means in Nielsen's limits, Apple flashlight details, backdrop blur size, color-blind prevalence in India, and the consensus items where tools agreed.

## Honest gaps
- Qwen was blocked by a CAPTCHA and was not used.
- Copilot was skipped.
- The Grok answer was cut off.
- Kimi covered perception only.
- Gemini answers were much shorter than the others.
- Not every sentence of every answer was audited line by line; only the load-bearing numbers and the disagreements were.

## Images
`images/` holds three reference concepts generated in ChatGPT: premium glass, flowy top bar, and an animation storyboard.

These images are research concepts, not the final PANOPTES UI or an approved visual direction.
