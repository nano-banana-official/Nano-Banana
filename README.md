# Nano Banana (Gemini 2.5 Flash Image)

Nano Banana is Google's Gemini image generation and editing model, known for consistent characters and natural-language edits.

> **Try Nano Banana online →** [https://banana-nano.co](https://banana-nano.co?utm_source=github&utm_medium=ugc&utm_campaign=nano-banana-official&utm_content=readme-top&utm_term=tier-b)

Nano Banana is the public nickname for Google's Gemini image models. The name first appeared in August 2025 as an anonymous entry on the LMArena image-editing leaderboard, where an unlabelled model called "nano-banana" outscored every other editor. Google later confirmed it was Gemini 2.5 Flash Image and shipped it under that name in the Gemini app, the Gemini API and Vertex AI. The nickname stuck, and Google now uses it officially: Nano Banana Pro is the consumer name for Gemini 3 Pro Image, and Nano Banana 2 is the name for the Gemini 3.1 Flash Image release.

The model is built by Google DeepMind on the Gemini multimodal stack rather than as a separate diffusion model, which is why it can accept text, one or several images and multi-turn instructions in the same conversation. It is best known for three things: keeping a person, pet or product visually consistent across edits and re-generations; performing targeted local edits ("remove the car", "change the shirt to red", "put this sofa in this room") from plain-language prompts without masks; and blending several reference images into one scene. The Pro tier adds high-resolution output, far better in-image text rendering and grounding in Google Search for factual visuals such as infographics.

In the market it sits against OpenAI's GPT Image models, Black Forest Labs' FLUX.1 Kontext, ByteDance's Seedream and Alibaba's Qwen-Image-Edit. Nano Banana's differentiators are speed on the Flash tier, editing fidelity, the reach of the Gemini distribution (it is the default image tool in the Gemini app, Google Search AI Mode, Google Slides and Vids, and Adobe Firefly and Photoshop) and every output carrying an invisible SynthID watermark.

## Contents

- [What Nano Banana (Gemini 2.5 Flash Image) can do](#what-nano-banana-gemini-2-5-flash-image-can-do)
- [Versions](#versions)
- [How to access Nano Banana (Gemini 2.5 Flash Image)](#how-to-access-nano-banana-gemini-2-5-flash-image)
- [Prompt examples](#prompt-examples)
- [Nano Banana (Gemini 2.5 Flash Image) vs alternatives](#nano-banana-gemini-2-5-flash-image-vs-alternatives)
- [Pricing](#pricing)
- [FAQ](#faq)
- [Links](#links)

## What Nano Banana (Gemini 2.5 Flash Image) can do

- Text-to-image generation with world knowledge from the Gemini model family; the Pro tier can ground prompts in Google Search for accurate diagrams, maps and infographics.
- Mask-free, prompt-based local editing: add, remove or replace objects, change backgrounds, restyle clothing, recolor, relight, without manually selecting regions.
- Character and product consistency: the same face, pet, mascot or item is preserved across multiple edits and across new scenes.
- Multi-image fusion: Gemini 2.5 Flash Image accepts up to 3 input images; Nano Banana Pro accepts up to 14 reference images and can hold up to 5 people consistent in one output.
- Multi-turn conversational editing: refinements are applied on top of the previous result inside the same chat or API session.
- Ten output aspect ratios (1:1, 2:3, 3:2, 3:4, 4:3, 4:5, 5:4, 9:16, 16:9, 21:9); Nano Banana Pro outputs at 1K, 2K or 4K.
- Legible text in images: the Pro tier renders headlines, labels, packaging copy and multilingual text with far fewer errors than the Flash tier, and can translate text inside an existing image.
- Style transfer and photo restoration: apply the texture or palette of one image to another, colorize or repair old photos, produce sketch-to-render and floor-plan-to-photo results.

Known limitations: the Flash tier outputs at roughly 1024 px on the long side and struggles with small or dense text; the Pro tier is slower and considerably more expensive per image. All outputs carry a SynthID watermark and, on the consumer side, a visible Gemini sparkle mark that cannot be disabled. Google's safety filters block many prompts involving real public figures, minors, and some violent or sexual content, and the model sometimes drifts on exact spatial instructions ("move the lamp 10 cm left"). It cannot generate video; that is handled by Veo.

## Versions

| Version | Released | Notes |
|---|---|---|
| Gemini 2.5 Flash Image (Nano Banana) | 2025-08 | First release; appeared anonymously on LMArena as nano-banana, then shipped as gemini-2.5-flash-image-preview. Native 1024 px output, up to 3 input images, SynthID watermark. |
| Gemini 2.5 Flash Image GA | 2025-10 | Stable model ID gemini-2.5-flash-image; adds the ten selectable aspect ratios and general availability on Vertex AI. |
| Nano Banana Pro (Gemini 3 Pro Image) | 2025-11 | Built on Gemini 3 Pro with a thinking step; 1K/2K/4K output, up to 14 reference images, Google Search grounding, much better text rendering. |
| Nano Banana 2 (Gemini 3.1 Flash Image) | 2026-02 | Flash-tier successor that brings much of the Pro quality and higher resolution to the faster, cheaper model. |

## How to access Nano Banana (Gemini 2.5 Flash Image)

Nano Banana is a hosted, closed model. Official ways to use it:

- Gemini app (web, Android, iOS): pick the image tool or simply attach a photo and describe the edit. Free accounts get a limited daily quota of Flash generations; Google AI Pro and AI Ultra subscribers get higher limits and access to Nano Banana Pro.
- Gemini API via Google AI Studio: model IDs `gemini-2.5-flash-image` (Flash) and `gemini-3-pro-image-preview` (Pro); AI Studio has a free tier with rate limits, paid usage is billed per output image.
- Vertex AI for Google Cloud customers, with enterprise controls and regional endpoints.
- Integrated surfaces: Google Search AI Mode, Google Slides, Vids and Workspace, Adobe Firefly and Photoshop, and third-party hosts such as fal.ai, Replicate, OpenRouter and Freepik that resell the API.

The Gemini app and API are not available in every country and the consumer quota resets daily; Pro-tier image generation also requires a paid Google AI plan. If you want to test the model without a Google account or a subscription, [Nano Banana](https://banana-nano.co) offers pay-per-generation access with no waitlist.

**Fastest way to try it:** [Try Nano Banana online](https://banana-nano.co?utm_source=github&utm_medium=ugc&utm_campaign=nano-banana-official&utm_content=readme-access&utm_term=tier-b) — no waitlist, runs in the browser.

## Prompt examples

**Product photo relight**

```text
Use the attached photo of the ceramic mug. Keep the mug exactly as it is, including the logo. Place it on a wet slate countertop at golden hour, soft window light from the left, shallow depth of field with a blurred kitchen behind, 3:2 aspect ratio, photorealistic.
```

**Consistent character in a new scene**

```text
Take the woman from the first image and put her in the cafe from the second image. She is sitting at the window table reading a paperback, same hairstyle, same green jacket, natural overcast daylight, candid documentary photography style.
```

**Infographic with text (Pro)**

```text
Create a clean vertical infographic titled 'How Espresso Extraction Works' with four numbered steps: Grind, Tamp, Pressure, Crema. Each step has a short one-line caption and a flat-style icon. Muted cream background, dark brown text, legible sans-serif typography, 9:16.
```

**Mask-free object removal**

```text
Remove the two people standing on the right side of the beach photo and fill the area with matching sand and waves. Keep everything else identical, including the lighting and the horizon line.
```

**Sketch to render**

```text
Turn this pencil sketch of a two-storey house into a photorealistic architectural render. Cedar cladding, black window frames, late-afternoon sun, a gravel driveway and a maple tree in the front yard, 16:9.
```

## Nano Banana (Gemini 2.5 Flash Image) vs alternatives

| Model | Max resolution | Editing / references | Text rendering | Access | Price tier |
|---|---|---|---|---|---|
| Nano Banana (Gemini 2.5 Flash Image) | ~1024 px | Prompt-based edits, up to 3 input images | Fair | Gemini app, Gemini API, Vertex AI | Low (roughly a few cents per image) |
| Nano Banana Pro (Gemini 3 Pro Image) | 4K | Up to 14 references, Search grounding | Strong | Gemini app (paid), Gemini API, Vertex AI | Medium-high |
| GPT Image 1.5 (OpenAI) | ~1536 px | Prompt-based edits with masks, multiple inputs | Strong | ChatGPT, OpenAI API | Medium |
| FLUX.1 Kontext (Black Forest Labs) | ~1 MP | Single-reference editing, open Dev weights | Fair | BFL API, self-hosted Dev, fal, Replicate | Low |
| Seedream 4.0 (ByteDance) | 4K | Multi-reference generation and editing | Good | Dreamina, Volcano Engine / BytePlus API, fal | Low-medium |

The Flash tier of Nano Banana is the fastest and cheapest of the group and is the strongest at conversational editing with a preserved subject, while GPT Image and Nano Banana Pro trade speed for higher resolution and dependable typography. FLUX.1 Kontext is the only option with downloadable weights, and Seedream 4.0 is the closest competitor on multi-reference composition and 4K output.

## Pricing

As of the last public information, Google bills Gemini 2.5 Flash Image on the Gemini API per output image, at a price that works out to a few US cents per 1024 px image (Google quotes it as roughly $0.039 per image, derived from a per-token rate of $30 per million output tokens). Nano Banana Pro is priced higher per image and by resolution, with 4K output costing more than 1K/2K. In the Gemini app the Flash tier is free with a daily cap, and Nano Banana Pro requires a Google AI Pro or AI Ultra subscription. Vertex AI uses the same per-image model with enterprise billing. Check the Gemini API pricing page for current figures because the numbers have changed several times since launch.

If you would rather not commit to a Google plan, [Nano Banana](https://banana-nano.co) provides pay-per-generation access, so you pay only for the images you actually produce.

## FAQ

**What is Nano Banana?**

Nano Banana is the nickname and now official product name for Google's Gemini image generation and editing models, starting with Gemini 2.5 Flash Image in August 2025. It is known for consistent characters, mask-free editing and multi-image fusion.

**Is Nano Banana free?**

Partly. The Flash tier is free in the Gemini app with a daily generation limit, and Google AI Studio has a limited free tier for the API. Nano Banana Pro and higher quotas require a paid Google AI plan or paid API usage.

**Is there a Nano Banana API?**

Yes. It is the Gemini API model gemini-2.5-flash-image, with gemini-3-pro-image-preview for Nano Banana Pro, available through Google AI Studio and Vertex AI, and resold by hosts such as fal.ai, Replicate and OpenRouter.

**Does Nano Banana have an official GitHub repository?**

No. Nano Banana is a closed, hosted model and Google has not released weights or an official repository. This page collects publicly available information about it.

**How do I try Nano Banana online?**

Open the Gemini app and attach or describe an image, or use Google AI Studio for the API. For pay-per-generation access with no account or waitlist, use https://banana-nano.co.

**What are the limits of Nano Banana?**

The Flash tier outputs at about 1024 px and is weak on small text; the Pro tier goes to 4K but is slower and costs more. All images carry a SynthID watermark, safety filters block some subjects, and the model does not generate video.

**What is the difference between Nano Banana and Nano Banana Pro?**

Nano Banana (Gemini 2.5 Flash Image) is the fast, low-cost tier with up to 3 input images and 1K output. Nano Banana Pro (Gemini 3 Pro Image) adds a reasoning step, 2K and 4K output, up to 14 reference images, Google Search grounding and far better text rendering.

## Links

- [Gemini image generation (official)](https://gemini.google/overview/image-generation/)
- [Gemini API image generation docs](https://ai.google.dev/gemini-api/docs/image-generation)
- [Google AI Studio](https://aistudio.google.com/)
- [Try Nano Banana online](https://banana-nano.co)

---

*This is an independent, community-maintained information repository about Nano Banana (Gemini 2.5 Flash Image). It is not affiliated with, endorsed by, or sponsored by Google DeepMind. All trademarks belong to their respective owners. Corrections welcome via issues.*
