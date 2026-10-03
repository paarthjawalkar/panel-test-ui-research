# Panel Test - UI / Perception / Premium research
Prepared overnight Oct 2-3, 2026 for Paarth Jawalkar.
Audience: Paarth, any AI model that reads this later, any human. Everything here is free-tier research. No monetization.

## 0. How to read this
- Method: one chat per topic, one project ("Panel Test") per tool. Same prompt per topic to every AI. Then outside verification on web sources for load-bearing numbers.
- Tools that answered: ChatGPT (Go plan), Perplexity (free), Claude Sonnet via arena.ai (free), DeepSeek, Gemini Pro (notebook "Panel Test"), Kimi (perception only), Grok (flowy, truncated).
- Gaps: Qwen blocked by a slider CAPTCHA (not solved on purpose). Copilot skipped per Paarth. Claude came from arena.ai, UI topics only. Grok answer was cut off. Kimi did perception only. Gemini answers are shorter (8-15k chars vs 40-58k elsewhere).
- Honest limit: raw answers total ~1.7 MB. I cross-checked the load-bearing numbers and the places where sources disagreed. I did NOT line-by-line audit every sentence of every answer. Raw answers are not included in this public repository.
- Interpretation rule: a number counts as "verified" only if I opened a primary or authoritative page (paper abstract, Apple/W3C/MDN docs, source code). "AI said it" alone is marked UNVERIFIED.

## 1. Topic findings (with the verified anchors)
### 1.1 Brain and learning
- Working memory: Miller's 7 plus/minus 2 is mostly misapplied; Cowan's ~4 chunks is the more accurate capacity (Claude, ChatGPT, DeepSeek, Gemini all agree). Chunking, cognitive load theory, split-attention, worked examples, predictive processing all covered.
- Unrehearsed short-term memory decays fast: Peterson and Peterson 1959, 24 students, trigrams, recall ~80% at 3 s to under 10% at 18 s. VERIFIED: https://www.simplypsychology.org/peterson-peterson.html and original https://psycnet.apa.org/doiLanding?doi=10.1037/h0049234
- "8 second attention span / goldfish": myth (Claude, Gemini). 
- Raw: chatgpt_brain, pplx_brain, claude_brain, deepseek_brain, gemini_brain.

### 1.2 Perception (eye, brain, what people like, color-blind and defects)
- Retina: average ~4.6 million cones (range 4.08-5.2M), peak foveal cone density mean 199,000 per mm2 (range 100,000-324,000). VERIFIED Curcio et al 1990, J Comp Neurol 292:497-523: https://pubmed.ncbi.nlm.nih.gov/2324310/ and https://onlinelibrary.wiley.com/doi/10.1002/cne.902920402
- First impressions form in ~50 ms: Lindgaard, Fernandes, Dudek, Brown 2006, Behaviour and Information Technology 25(2):115-126. VERIFIED https://www.tandfonline.com/doi/abs/10.1080/01449290500330448
- Scene gist at 13 ms per picture: Potter, Wyble, Hagmann, McCourt 2014, Attention Perception and Psychophysics. VERIFIED https://pmc.ncbi.nlm.nih.gov/articles/PMC5328417/ . (This is detection of a named scene in rapid sequence, not "liking".)
- Aesthetic-usability: Kurosu and Kashimura CHI 95 https://dl.acm.org/doi/10.1145/223355.223680 ; Tractinsky, Katz, Ikar 2000 https://www.sciencedirect.com/science/article/abs/pii/S095354380000031X (both exist, VERIFIED).
- Curves preferred: Bar and Neta 2006, Psychological Science 17(8) https://pubmed.ncbi.nlm.nih.gov/16913943/ (exists; VERIFIED).
- Golden ratio: all five AIs call it design folklore, not a perceptual law.
- Color-vision deficiency (ChatGPT follow-up "from defects upward", full text: chatgpt_perception_cb2.txt): L and M opsin genes OPN1LW/OPN1MW sit in a tandem array on the X chromosome (Xq28), >98% sequence identity, so red-green defects are X-linked and male-dominant. S-opsin OPN1SW is on chromosome 7, so tritan defects are not X-linked. Complete achromatopsia is usually not an opsin-array problem.
- Prevalence: "8% of men, 0.5% of women" is Northern European. India numbers differ (section 2, contradiction 7).
- Also covered in the follow-up: optics, lens/presbyopia, cataract yellowing (short wavelengths lost), retina to cortex chain. Design framing: "two people can both say I can't read this glass UI for completely different physical reasons."
- Raw: chatgpt_perception, pplx_perception, claude_perception, ds_perception, kimi_perception, gemini_perception, chatgpt_perception_cb2.

### 1.3 Premium psychology
- Mechanisms all sources use: processing fluency, costly signaling, labor illusion, aesthetic-usability effect, consistency, 4/8pt spacing rhythm, optical sizing and tracking, tabular figures for live data, optical icon alignment, springs over linear easing.
- Apple lock-screen flashlight (his example): see contradiction 5 for what is documented and what is invented.
- "Liquid glass existed before Apple": DeepSeek lists Windows Vista Aero, iOS 7 blur, Windows Fluent acrylic (2017), macOS vibrancy (2014), Oppo/ColorOS frosted panels as earlier art. Apple's 2025 Liquid Glass adds real-time refraction (lensing), specular highlights that respond to device motion, adaptive tint (DeepSeek, Pplx). Dates/Oppo claim not independently verified beyond Apple's docs mention; treat Oppo-before-Apple as plausible, UNVERIFIED by me.
- Raw: chatgpt_premium, pplx_premium, arena_claude_premium, ds_premium, gemini_premium.

### 1.4 Displays and electronics
- Frame time: 60 Hz = 16.67 ms, 90 Hz = 11.11 ms, 120 Hz = 8.33 ms (arithmetic, 1000/Hz). 
- Panel tech, PWM dimming/flicker, burn-in, LTPO VRR, touch sampling vs refresh, finger-to-photon latency chain, gamma, HDR, nits and ambient light all covered by ChatGPT, Pplx, Claude, DeepSeek, Gemini.
- Color gamut size: contradiction 3.
- Raw: chatgpt_displays, pplx_displays, claude_displays, ds_displays, gemini_displays.

### 1.5 Flowy design (which, how much, where it stops)
- Claude's key point: "flowy" is six different technical things (springs, easing, shared-element, gesture-tracked, gradient/mesh, organic shape). A 20 s looping gradient and a 150 ms button press are both called flowy but share no mechanics. Budget them separately.
- Timing anchors: Nielsen 0.1 s / 1 s / 10 s limits https://www.nngroup.com/articles/response-times-3-important-limits/ (VERIFIED). Doherty 400 ms threshold is about system response, not animation length (Claude's scope warning).
- Springs: see contradiction 2 for verified defaults.
- Where it stops: DeepSeek and Pplx: duration budgets about 100-300 ms for common UI, 300-500 ms only for spatial changes; Disney squash-and-stretch is aesthetic, not proven functional. Blur and GPU cost: contradiction 6.
- Raw: chatgpt_flowy, pplx_flowy, claude_flowy, ds_flowy, gemini_flowy, grok_flowy (thin).

## 2. Contradictions and verdicts
1. Cone count: ChatGPT table said ~6.4M, others 4.6M. VERDICT 4.6M. 4.6M is Curcio 1990's direct count (4.08-5.2M). 6.4M cones (and 110-125M rods) is Osterberg 1935, still printed in textbooks (https://ncbi.nlm.nih.gov/books/NBK11556/ , https://www.webvision.pitt.edu/book/part-xiii-facts-and-figures-concerning-the-human-retina/). Newer method wins; ChatGPT's own prose later reconciles this. Rods: Curcio ~92M (78-107M).
2. Spring defaults: Claude said SwiftUI .spring default response 0.55. WRONG. Apple docs: response 0.5, dampingFraction 0.825 (https://developer.apple.com/documentation/swiftui/animation/spring(response:dampingfraction:blendduration:)). Claude's Framer/Motion default (stiffness 100, damping 10, mass 1) is CORRECT per the library source (https://github.com/motiondivision/motion/blob/cd531784/packages/motion-dom/src/animation/generators/spring.ts , https://motion.dev/examples/js-spring). Hand check: damping ratio = 10 / (2 x sqrt(100 x 1)) = 0.5, clearly underdamped, visible overshoot. A motion.dev doc page prints "stiffness default 1" in one place, which conflicts with the code; code wins. DeepSeek said Apple publishes no spring constants: partly wrong. Apple publishes API defaults, not the internal values of system animations.
3. Display P3 vs sRGB size: Pplx "~50% more colors by volume", Claude/DeepSeek "~45% vs ~35% of visible chromaticities", Apple WWDC17 "25% larger", WebKit "around 50% larger". VERDICT: not a real conflict, different metrics. About 25% is the 2D xy area ratio (https://developer.apple.com/videos/play/wwdc2017/821/), about 50% is 3D volume (https://webkit.org/blog/10042/wide-gamut-color-in-css-with-display-p3/ , https://colormanagement.guide/en/working-spaces/display-p3/). Say both numbers with their metric. Pplx handled it best.
4. "1 second" meaning: Gemini called Nielsen's 1.0 s the limit of short-term memory maintenance. WRONG label. Nielsen's 1 s = user's flow of thought stays uninterrupted (perception of response). Memory decay is Peterson 1959 (~18 s). VERDICT: DeepSeek/Claude right, Gemini mislabeled.
5. Apple flashlight details: Gemini: press needs "roughly 300-500 ms". DeepSeek: "predictive touch expansion" and force-driven visuals. Pplx: bottom-left, small icon with generous target, HIG transient haptic. VERDICT: documented facts only: bottom-left, press-and-hold (https://support.apple.com/en-us/105001); hold time is user-adjustable Fast/Slow in Haptic Touch settings (https://support.apple.com/guide/iphone/touch-iph77bcdd132/13.0/ios/13.0), so 300-500 ms is not a fixed Apple constant; WWDC19 session 520 calls the lock-screen flashlight "a very high sharpness haptic" (https://developer.apple.com/videos/play/wwdc2019/520/); HIG uses the flashlight tap as a "transient" haptic example (https://developer.apple.com/design/human-interface-guidelines/playing-haptics). DeepSeek's "predictive touch expansion" has no source. UNVERIFIED, do not repeat. Pplx closest to the sources.
6. Backdrop blur size: Gemini 24-40 px for legibility; DeepSeek max 16 px on mobile and under 30% of screen; Apple's real radius is not public. Neither has a measurement behind it. VERDICT: no universal px value. CSS blur(r) uses r as the Gaussian standard deviation (https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/filter-function/blur). Cost scales with area and radius, so profile on the target phone (target device, Chrome DevTools Performance). 120 Hz budget math is right (8.33 ms); the claimed 3-10 ms and >25 ms figures are UNVERIFIED.
7. Color-blind prevalence: "8% of men" repeated by several sources as universal. It is Northern European. India: Kanchipuram school screen of 74,986 boys = 2.76% (https://pmc.ncbi.nlm.nih.gov/articles/PMC8482944/); North India six populations male 7.52%, female 0.83%, range 2.5-7.79% by population (https://pmc.ncbi.nlm.nih.gov/articles/PMC3595632/); another screen cites 2.98% (https://www.jcdr.net/articles/PDF/17138/60162_CE(Vi)_F(SHU)_PF1(SC_KM)_PFA(SC_KM)_PN(KM).pdf). VERDICT: use "roughly 2.5% to 8% of Indian males depending on population"; still design for the worst case.
8. Attention/golden ratio and other consensus items: no contradiction (all agree).

## 3. What this means for PANOPTES UI
1. Hierarchy first, glass second: first impression is ~50 ms and mostly luminance and layout, so the dark globe plus clear contrast levels matter more than any glass effect.
2. Contrast is worst-case: translucent panel over bright terrain or dark ocean. Test text contrast over both extremes (DeepSeek rule: WCAG 4.5:1 normal text, 3:1 large). Protective tint behind blur (Gemini example: L about 0.10, alpha about 0.72, untested).
3. Never rely on hue alone: red-green deficiency is common (2.5-8% of men, depending on population). Pair color with shape, label, luminance difference. Blue/yellow axis also needs a check (tritan, rarer, and cataract/age shift).
4. Keep motion in three buckets: micro feedback 100-200 ms, panel moves 200-300 ms, spatial context change 300-500 ms. Use springs for gesture release (SwiftUI default response 0.5, damping 0.825 is a good reference; Motion default 100/10/1 overshoots, damping ratio 0.5, so raise damping for a calmer feel).
5. Blur and the globe compete for the same GPU. Set a blur budget by profiling on the real phone, not a number from an AI.
6. Premium = consistency + small verified details: 4/8pt grid, tabular figures for live data, optical icon alignment, haptics on the same events every time. Do not copy unsourced "Apple secrets".
7. Dark UI is fine and OLED-friendly for burn-in, but fixed bright elements in the same position for hours are a burn-in risk (DeepSeek: unverified numbers).
8. Display P3 is allowed but keep a sRGB-safe palette: saturation that "pops" on P3 phones can become overly flashy (his Google-flashy negative example).

## 4. Files
Reference images are in `images/`: 3 premium-UI concepts generated in ChatGPT (ref1_premium_glass, ref2_flowy_topbar, ref3_animation_storyboard). The raw per-tool answers are not published in this repo.
