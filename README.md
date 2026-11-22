# Awesome GPT Image API 🎨 — Prompts, Variants & One-Call Image Generation

> The most complete open guide to **OpenAI GPT Image — the multimodal image model (GPT Image 2.6 · 2.5 · 2 · 1.5, text-to-image + edit)** — a community prompt library and a single API to run every variant.

<p align="center">
  <a href="https://wavespeed.ai/gpt-image-2-6-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api"><img src="https://img.shields.io/badge/▶_Run_GPT_Image_2.6-Get_API_Key-00E5FF?style=for-the-badge&labelColor=0B0B0F" alt="Run GPT Image 2.6"></a>
  <a href="https://wavespeed.ai/gpt-image-2-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api"><img src="https://img.shields.io/badge/GPT_Image_2.5-Try_Now-7C3AED?style=for-the-badge&labelColor=0B0B0F" alt="GPT Image 2.5"></a>
</p>

<p align="center">
  <b>🌊 Powered by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api">WaveSpeedAI</a> — serverless GPT Image API, pay-as-you-go, zero cold starts.</b><br>
  <a href="https://wavespeed.ai/gpt-image-2-6-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api"><b>→ Get a GPT Image 2.6 API key</b></a> &nbsp;·&nbsp; <a href="https://wavespeed.ai/gpt-image-2-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api"><b>→ Try GPT Image 2.5</b></a>
</p>

<p align="center">
  🖥️ <b>No code?</b> Generate in your browser (no setup, free to start) → <a href="https://wavespeed.ai/image-generator?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api"><b>WaveSpeedAI Image Generator</b></a>
</p>

---

> **Generate right now**
> ```bash
> npm i -g @wavespeed/cli && wavespeed login
> wavespeed run openai/gpt-image-2.6-flare/text-to-image -p "your prompt"
> ```
> No GPU, no cold start — the same endpoint powers every prompt below.

---

## 📖 Contents
1. [What is GPT Image?](#what-is-gpt-image)
2. [Run it via API](#run-it-via-api)
3. [Model Variants](#model-variants)
4. [Prompt Library](#prompt-library) — 12 community prompts
5. [Related Model Guides](#related-model-guides)
6. [Contributing](#contributing)

---

## What is GPT Image?

**GPT Image** is OpenAI's multimodal image generation and editing model, strong on prompt comprehension, in-image text, and reference-guided edits. WaveSpeedAI serves **GPT Image 2.6** in two tiers — Flare for fast everyday generation and Sunburst for higher fidelity — plus GPT Image 2.5, 2 and 1.5, each with text-to-image and edit.

---

## Run it via API

One endpoint, submit + poll. Swap the model path for any variant below.

```bash
curl -s -X POST "https://api.wavespeed.ai/api/v3/openai/gpt-image-2.6-flare/text-to-image" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY" -H "Content-Type: application/json" \
  -d '{"prompt": "A vintage travel poster of Mars colony, bold typography, retro-futurism", "aspect_ratio": "16:9"}'
# → {"data": {"id": "<prediction_id>"}}

curl -s "https://api.wavespeed.ai/api/v3/predictions/<prediction_id>/result" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY"
# → status: completed → outputs: ["<url>"]
```

**[→ Get your GPT Image 2.6 API key](https://wavespeed.ai/gpt-image-2-6-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api)** · pay-as-you-go, live pricing on each model page.

**Python wrapper:** [gpt-image-2.6-api](https://github.com/WaveSpeedAI/gpt-image-2.6-api) — one typed function per GPT Image 2.6 endpoint, built on the official SDK.

---

## Model Variants

All variants open in-browser with a copy-paste API snippet.

### GPT Image 2.6 — flagship &nbsp;[▶ API](https://wavespeed.ai/gpt-image-2-6-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api)
[flare text-to-image](https://wavespeed.ai/models/openai/gpt-image-2.6-flare/text-to-image?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api) · [flare edit](https://wavespeed.ai/models/openai/gpt-image-2.6-flare/edit?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api) · [sunburst text-to-image](https://wavespeed.ai/models/openai/gpt-image-2.6-sunburst/text-to-image?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api) · [sunburst edit](https://wavespeed.ai/models/openai/gpt-image-2.6-sunburst/edit?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api)

### GPT Image 2.5 &nbsp;[▶ API](https://wavespeed.ai/gpt-image-2-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api)
[flare text-to-image](https://wavespeed.ai/models/openai/gpt-image-2.5-flare/text-to-image?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api) · [flare edit](https://wavespeed.ai/models/openai/gpt-image-2.5-flare/edit?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api) · [sunburst text-to-image](https://wavespeed.ai/models/openai/gpt-image-2.5-sunburst/text-to-image?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api) · [sunburst edit](https://wavespeed.ai/models/openai/gpt-image-2.5-sunburst/edit?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api)

### GPT Image 2 &nbsp;[▶ API](https://wavespeed.ai/gpt-image-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api)
[text-to-image](https://wavespeed.ai/models/openai/gpt-image-2/text-to-image?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api) · [edit](https://wavespeed.ai/models/openai/gpt-image-2/edit?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api)

### GPT Image 1.5
[text-to-image](https://wavespeed.ai/models/openai/gpt-image-1.5/text-to-image?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api) · [edit](https://wavespeed.ai/models/openai/gpt-image-1.5/edit?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api)

> Full catalog: **[wavespeed.ai/gpt-image-2-6-api](https://wavespeed.ai/gpt-image-2-6-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api)**

---

## Prompt Library

12 prompts curated from the GPT Image creator community. Credit stays with the original author. Fill in `{...}` placeholders.

### 1. E-commerce Main Image - Miniature Diorama Skincare Advertisement )
*by [@Strength04_X](https://x.com/Strength04_X)*

```
A hyper-realistic miniature diorama product advertisement featuring an oversized luxury skincare pump bottle labeled "LUXEVEIL Skin Science - Radiance Nourishing Body Lotion" in cream/beige with a polished gold pump top, placed on a circular platform. Tiny figurine construction workers dressed in yellow coveralls and white hard hats swarm around the bottle climbing scaffolding, painting the bottle with rollers, operating a tower crane, working near industrial tanks and pipework, and unloading a miniature flatbed truck. The scene includes metal scaffolding structures, industrial silos, orange traffic cones, wooden barricades, and storage barrels. The overall color palette is warm beige, cream, gold, and mustard yellow. Studio photography style with soft diffused lighting, no shadows, clean beige background. The concept metaphorically shows workers "crafting" or "building" the perfect lotion. Tilt-shift miniature aesthetic, ultra-detailed, commercial product photography, 8K resolution, photorealistic CGI render.
```

### 2. Burger hero image plus 9-cell ad storyboard )
*by [@Gdgtify](https://x.com/Gdgtify)*

```
Prompt 1: Create a cinematic hero image of a gourmet cheeseburger on a dark stone surface with glossy brioche bun, melted cheese, crisp lettuce, tomato, grilled patty, sauce, realistic texture, appetizing steam, warm side light, shallow depth of field, premium food commercial style, no text/logos/watermark.

Prompt 2: Create a 9-cell hybrid keyframe-to-transition storyboard sheet for a 15-second gourmet burger ad, moving from empty surface to ingredient assembly to final macro hero shot. Use large S cells and smaller T cells, motion arrows, ghosted ingredient positions, steam, sauce trails, and camera push-in icons. Style: premium food commercial, warm lighting, rich texture, appetizing, cinematic, minimal labels only. No logos, no watermark.
```

### 3. 3D Pixel Food Transformation )
*by [@iamaiistudio](https://x.com/iamaiistudio)*

```
A minimalist food photograph featuring a single [FOOD] on a clean matte white surface, caught mid-transformation into a 3D pixel art style. The left half is perfectly photorealistic while the right half dissolves into large floating geometric cubes, each cube exposing the food's vibrant colors, textures, and inner details. Soft studio lighting, gentle shadows, shallow depth of field, hyperrealistic meets geometric abstraction, subtle motion blur on the cubes. High resolution cinematic close-up composition.

Full prompt:
```

### 4. Ancient Palace Perfume Ad )
*by [@iamaiistudio](https://x.com/iamaiistudio)*

```
Full prompt:

Ancient Chinese palace perfume advertisement inspired by the legendary dancer Zhao Feiyan. A bronze bottle with gold-inlaid twisting lotus vines. Mysterious, cold, and haunting imperial harem atmosphere. Vertical portrait format, 9:16 ratio.
```

### 5. Plush Soda Can Product Shot )
*by [@iamaiistudio](https://x.com/iamaiistudio)*

```
prompt:

A soda can featuring the label [BRAND NAME], constructed entirely from soft, colorful plush material, centered against a matching plush background in [BRAND NAME]'s brand colors.

Pop Art and Memphis-inspired style, vibrant and premium at the same time.

Crisp studio lighting that highlights every fiber, the plush texture, and the tactile softness of the material.

Razor-sharp focus, vivid color saturation, clean shadows, sleek commercial product photography, minimalist composition, ultra-high resolution.
```

### 6. Lightning Storm Supercar Ad )
*by [@iamrealsnow](https://x.com/iamrealsnow)*

```
Sports Car Made of Lightning
Prompt: Supercar emerging from a storm cloud, body formed entirely from blue lightning bolts, wet reflective road, thunder exploding in background, cinematic action advertising, high-speed energy trails, ultra-detailed automotive render, luxury commercial photography, 8K.
```

### 7. Miniature Brand Universe Shoe )
*by [@AIwithAliya](https://x.com/AIwithAliya)*

```
A high-performance running shoe transformed into a miniature brand universe. The shoe is the hero character, surrounded by floating speed trails, miniature running tracks, energetic mascot companions, stopwatch icons, clouds, and dynamic sports-inspired elements. Oversized bold typography integrated into the scene. Clean commercial 3D rendering, pastel orange, white, and gray color palette derived from the product, premium packaging aesthetics, soft gloss, graphic backgrounds, floating platforms, collectible toy-like charm. Modern consumer branding, cute yet premium, highly shareable social-media campaign visual, rich detail, centered composition, studio quality.
```

### 8. Floral Serum Product Shot )
*by [@iamaiistudio](https://x.com/iamaiistudio)*

```
Minimalist studio product photography, a small transparent glass facial oil dropper bottle with a black rubber pipette cap, containing pale pink serum with suspended dried pink floral elements, centered on a natural raw wooden block with visible grain and split texture. Tall matte white skincare box on the left labeled "HUILE ÉCLAT VISAGE" with clean black typography and subtle logo near the bottom. Clear cylindrical glass vase on the right filled with water and thin stems of dried pink gypsophila extending upward. Composition rests on a smooth matte pastel pink surface against a matching seamless pink studio background. Strong directional soft light from the left casts long natural-style shadows of the flowers onto the background, with gentle highlights on the glass, subtle reflections on the serum bottle, and soft texture on the wooden block. Straight-on tabletop camera angle, all objects in sharp focus. Color palette: blush pink, soft rose, warm light wood, clean white, transparent glass. Premium Scandinavian minimalist skincare aesthetic, ultra-realistic, studio-grade.

full prompt:
```

### 9. Spicy Chili Chutney Product Shot )
*by [@iamaiistudio](https://x.com/iamaiistudio)*

```
Overhead shot of a glass jar of spicy tomato chili chutney on a dark stone surface, surrounded by whole red tomatoes, tomato halves, fresh red chili peppers, black peppercorns, and a small wooden bowl with chutney and a spoon. Warm earthy backdrop, soft directional light, deep rich shadows, high contrast, clean minimal styling, commercial product photography, ultra-detailed, 4K.
```

### 10. Levitating Food Photography Set )
*by [@iamaiistudio](https://x.com/iamaiistudio)*

```
A professional studio food photography series showcasing deconstructed dishes captured mid-air in dramatic high-speed levitation. Set against a seamless dusty pink backdrop with soft, even studio lighting, the ingredients burst and float in dynamic formations. Featured dishes include a suspended tiramisu with its components (scoops of gelato, ladyfingers, mascarpone cream, and coffee beans) hovering in the air, borscht elements (beets, rye bread slices, fresh herbs) floating above a ceramic bowl of soup resting on a wooden board, and a sourdough toast topped with mashed avocado and a runny poached egg caught mid-split. Fine details like flying crumbs, spice particles, scattered herbs, and liquid droplets should be razor-sharp with a shallow depth of field. Soft shadows fall beneath the main suspended elements.
```

### 11. Luxury chocolate campaign system )
*by [@SPEEDAI07](https://x.com/SPEEDAI07)*

```
Create a premium, square (1:1) product advertisement for a fictional luxury chocolate brand called Noirvelle Chocolat, inspired by high-end chocolate brands. The ad should feel like a high-end editorial campaign, combining luxury food photography, refined packaging design, and cinematic lighting. Use matte black wrapper, subtle gold foil, elegant serif typography, and realistic product rendering. Generate flavor variants such as Blood Orange Noir, Salted Pistachio Muse, and Raspberry Ember with distinct mood, color palette, ingredients, headline, and supporting copy. Keep the chocolate bar as hero centerpiece with subtle reflections, shallow depth of field, luxury minimalism, and a small CTA: "Shop the drop."
```

### 12. Luxury Fragrance Campaign Portrait )
*by [@amynys](https://x.com/amynys)*

```
Transform the uploaded portrait into a luxurious cinematic fragrance poster inspired by the dark seductive elegance of a high-fashion perfume campaign. Preserve her exact facial features, warm skin tone, confident expression, wavy brunette hair, and recognizable identity. Style her as a mysterious femme fatale with soft glossy lips, luminous skin, subtle smoky eyes, and an intense captivating gaze.

Dress her in a black satin slip dress with delicate lace trim and a glamorous faux fur wrap slipping off her shoulders. Place her inside a moody Parisian-inspired luxury interior with black reflective walls, gold rim lighting, deep shadows, cinematic contrast, and sensual ambient lighting. Add elegant reflections and depth for a premium editorial look.

Include a sleek black perfume bottle inspired by a luxury noir fragrance aesthetic near the foreground. Use refined minimalist typography in a luxury fashion-ad style with dramatic spacing and premium composition. Add a tagline such as: “She doesn’t follow. She leaves a trace.”

The overall mood should feel seductive, mysterious, powerful, feminine, cinematic, timeless, and ultra-luxurious — like a Chanel Coco Noir campaign directed by a Hollywood cinematographer. High detail, photorealistic skin texture, glossy highlights, rich blacks, warm gold accents, magazine-quality fashion photography, 8K luxury editorial finish.
```

*Add yours via a PR — keep the original author's credit. See [Contributing](#contributing).*

---

## Related Model Guides
Part of the WaveSpeedAI **Awesome Model** series — one guide per frontier model, all runnable through one API:

- 🎬 [awesome-seedance-api](https://github.com/WaveSpeedAI/awesome-seedance-api) — ByteDance Seedance video
- 🌊 [awesome-wan-api](https://github.com/WaveSpeedAI/awesome-wan-api) — Alibaba Wan video
- ⚡ [awesome-minimax-h3-api](https://github.com/WaveSpeedAI/awesome-minimax-h3-api) — MiniMax Hailuo H3 video
- 🎞️ [awesome-kling-api](https://github.com/WaveSpeedAI/awesome-kling-api) — Kling video
- 🖼️ [awesome-seedream-api](https://github.com/WaveSpeedAI/awesome-seedream-api) — ByteDance Seedream image
- 🎨 [awesome-gpt-image-api](https://github.com/WaveSpeedAI/awesome-gpt-image-api) — OpenAI GPT Image *(this repo)*
- 🍌 [awesome-nano-banana-api](https://github.com/WaveSpeedAI/awesome-nano-banana-api) — Google Nano Banana image

---

## Contributing
PRs welcome:
1. Reusable prompts (`{placeholders}` for swappable parts).
2. **Credit the original author** with a link.
3. No output images unless you own and can license them.

## License
[CC0-1.0](LICENSE) — text & prompts are free to use. Model outputs follow the model provider's and [WaveSpeed](https://wavespeed.ai)'s terms.

---
<p align="center"><sub>Maintained by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api">WaveSpeedAI</a> — the fastest way to run frontier image & video models via one API. <a href="https://wavespeed.ai/gpt-image-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-gpt-image-api"><b>Run GPT Image →</b></a></sub></p>
