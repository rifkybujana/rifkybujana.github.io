# Rifky Bujana Bisri — Personal Blog

## Project Overview

A minimal personal blog styled after [brandonrohrer.com/blog.html](https://brandonrohrer.com/blog.html). Ultra-plain HTML, no frameworks, no build step. Georgia serif, max-width 680px, default browser aesthetics. The site is a collection of pages about Rifky's projects and a learning series on SAM3.

## File Structure

```
index.html                              # Home page — motto, intro, public projects, learning series index
sam3/01-machines-eyes.html              # Chapter 1: Machine's Eyes — how machines see images
sam3/02-the-language-of-numbers.html    # Chapter 2: The Language of Numbers — one-hot, dot product, matmul, softmax, attention
sam3/03-what-is-sam3.html               # Chapter 3: What is SAM3? — SAM lineage and architecture overview
```

All pages are flat static HTML files. No CSS framework, no JS. Styles are inlined in each page's `<style>` block.

## Design Rules

- **Font**: Georgia, 'Times New Roman', serif
- **Layout**: max-width 680px, centered, 1.2em horizontal padding
- **Links**: #1a0dab unvisited, #609 visited
- **Headings**: h1 for page title, h3 for sections on home, h2 for sections in articles
- **No em-dashes**. Use periods, commas, or short sentences instead.
- **No bullet points in prose**. Lists only for link collections (projects, chapter index).
- **Minimal formatting**. No bold, no italic except `.subtitle` class.
- **Breadcrumb** at top of article pages: `Home › Section`
- **Navigation** at bottom of article pages: previous/next links and home link

## Writing Style

- **Poetic and invitational**. Ask the reader to picture, suppose, feel. But vary the verbs — don't repeat "imagine."
- **Short paragraphs**. 2-4 sentences max.
- **Conversational**. Write like you're explaining to a smart friend, not lecturing.
- **No jargon without grounding**. Introduce technical terms through analogy first, then name them.
- **Section headings are evocative**, not academic. "Close your eyes" not "Introduction to Computer Vision."
- **First person singular** for the home page and personal context. Third person or second person ("you") for teaching content.

## Rifky's Info

- **Name**: Rifky Bujana Bisri
- **Motto**: Making AI Accessible to Anyone, Anywhere
- **Company**: None listed publicly (Rifky is exiting Kolosal due to direction misalignment; do not associate him with Kolosal as his employer/affiliation on this site)
- **Email**: rifky@kolosal.ai (will stop working after Kolosal exit — replacement TBD)
- **Pitch**: While others were in high school, Rifky built his country's best AI model — now he builds from silicon to shipped product.

## Public Projects

1. [Model Memory Calculator](https://github.com/KolosalAI/model-memory-calculator) — Single-file browser app that reads GGUF metadata and estimates RAM/VRAM usage. No server required.
2. [SAM3.c](https://github.com/rifkybujana/sam3.c) — Pure C implementation of Meta's Segment Anything Model 3. No Python, no framework dependencies.
3. [Kolosal AI Platform](https://github.com/KolosalAI/kolosal) — Fully local AI runtime in C++. Custom tensor library, inference engine, native UI. Runs on any device.
4. [IndoBERT QA](https://github.com/rifkybujana/indobert-qa) — IndoBERT Base fine-tuned on translated SQuAD v2.0. SOTA extractive QA for Bahasa Indonesia (2021).

## SAM3 From Scratch

A chapter-by-chapter walkthrough of building SAM3.c from scratch. Current chapters:

1. **Machine's Eyes** (`sam3/01-machines-eyes.html`) — How machines see. Pixels as numbers, filters, edges, objects, segmentation. Done.
2. **The Language of Numbers** (`sam3/02-the-language-of-numbers.html`) — One-hot encoding, dot products, matrix multiplication, softmax, attention. The math foundations. Done.
3. **What is SAM3?** (`sam3/03-what-is-sam3.html`) — SAM1 → SAM2 → SAM3 lineage. Text prompts, concept segmentation, architecture overview, motivation for C rewrite. Done.
4. **Tokenizer: Teaching Machines to Read** — Not yet written. How tokenizers break text into tokens for neural networks.

## Image Prompts (not yet generated)

All images should be in **rough crayon sketch style on aged cream paper, visible paper texture, uneven strokes, smudged edges, muted warm tones**. Specific prompts per page:

### blog.html
- Hero: "A single candle illuminating an open notebook in a dark room, pages filled with hand-drawn neural network diagrams, soft golden light bleeding into shadow. Rough crayon sketch on aged cream paper, visible paper texture, uneven strokes, smudged edges, muted warm tones with one accent of deep blue"

### machines_eyes.html
- Close your eyes: "A blindfolded marble statue in a dark gallery, thousands of tiny floating numbers reflected on its smooth surface. Rough crayon sketch on cream paper, heavy shading with charcoal-like strokes, numbers drawn in faint colored pencil, smudged and imperfect"
- Run your fingers: "Fingers pressing into sand and leaving ripples, but the sand is made of tiny glowing pixels dissolving at the edges. Rough crayon sketch, warm ochre and burnt sienna tones, pixels rendered as small uneven squares in wax crayon, paper grain showing through"
- Step back: "A cathedral seen from far away dissolving into brushstrokes, then into geometric shapes, then into points of light. Rough crayon sketch triptych on cream paper, left panel detailed, middle panel loose, right panel nearly abstract, heavy waxy texture throughout"
- The hardest question: "A porcelain vase shattering in slow motion, each fragment perfectly labeled with a different color of light, frozen mid-air. Rough crayon sketch, bold outlines in dark pencil, each shard filled with a different pastel crayon color, visible hand pressure variation"

### what_is_sam3.html
- Point at something: "A child's finger reaching toward a butterfly in a meadow, the butterfly glowing faintly as if it knows it has been chosen. Rough crayon sketch on cream paper, the meadow rendered in quick green strokes, the butterfly in careful detail with soft yellow and orange crayon, everything else loose and gestural"
- Then it learned to watch: "A long-exposure bird in flight, its path traced as a ribbon of light against a twilight sky. Rough crayon sketch, the bird drawn multiple times in overlapping positions like a flipbook, each copy slightly fainter, deep indigo and violet crayon for the sky, paper texture visible"
- Now it understands words: "A library where every book spine is a different real-world object, shoes, cups, umbrellas, and a single whispered word floats in the air between the shelves. Rough crayon sketch, warm brown and amber tones for the shelves, each object spine drawn in a different bright crayon color, the floating word in faint graphite"
- Why rewrite it in C: "A watchmaker's table, gears and springs laid bare under a magnifying glass, everything precise and naked, no case, no facade. Rough crayon sketch on cream paper, the gears drawn with careful mechanical precision in dark graphite, the table and background loose and smudged in warm brown crayon, contrast between control and chaos"

## Next Steps

- [ ] Generate images from prompts above and embed them into pages
- [ ] Write the Tokenizer chapter
- [ ] Add more chapters as SAM3.c implementation progresses
- [ ] Consider adding an RSS feed

---

## Diagram Style Guide

All architecture diagrams and technical documentation pages must follow these rules for visual consistency. The reference style is inspired by the GGUF format diagram: minimalist, clean, easy to understand, yet detailed. Think "technical reference poster", not "slide deck".

### Philosophy

- **Minimalist but detailed.** Show the real data: struct fields, tensor shapes, byte offsets, concrete values. Don't simplify away the numbers.
- **Flat design.** No gradients, no shadows, no blur, no 3D effects. Clean flat surfaces and thin borders.
- **Light mode only.** No dark mode. Do not include `@media (prefers-color-scheme: dark)` blocks.
- **Monospace for data, sans-serif for prose.** Code, shapes, field names, hex values use mono. Titles and descriptions use sans.
- **Dashed boxes for detail breakouts.** When a region needs annotation, use a `1.5px dashed` border box connected by a dashed leader line.
- **Color encodes category, not decoration.** Each color ramp maps to a semantic domain (e.g. purple = vision backbone, teal = features, coral = fusion). Stay consistent within a document.

### Page Layout

```css
body {
  font-family: var(--sans);
  color: var(--text);
  background: var(--bg);
  line-height: 1.5;
  padding: 40px 24px;
  max-width: 780px;    /* 860px for dense architecture docs */
  margin: 0 auto;
}
```

#### Header pattern

```html
<div style="font-size:13px;color:var(--text2)">Category / context label</div>
<div style="font-size:22px;font-weight:600;margin-bottom:20px">Main title</div>
```

For architecture docs with multiple sections:

```html
<div style="font-size:13px;color:var(--text3);margin-bottom:24px">848M params · NHWC · CPU + Metal</div>
<div class="toc">
  <a href="#overview">1. Overview</a> · <a href="#details">2. Details</a>
</div>
```

#### Section headings

```css
h2 { font-size: 16px; font-weight: 600; margin: 48px 0 4px; padding-bottom: 6px; border-bottom: 1px solid var(--border); }
h2 .num { color: var(--text3); font-weight: 400; margin-right: 4px; }
h3 { font-size: 14px; font-weight: 600; margin: 24px 0 4px; }
```

### Color System

9 color ramps. Each ramp has 4 CSS variables: `--{name}`, `--{name}-bg`, `--{name}-border`, `--{name}-text`. Light mode only.

#### Light mode values

| Ramp   | `--bg`    | `--border` | `--text`  | `--accent` | Use                          |
|--------|-----------|------------|-----------|------------|------------------------------|
| purple | `#EEEDFE` | `#AFA9EC`  | `#3C3489` | `#534AB7`  | Vision backbone, primary hl  |
| teal   | `#E1F5EE` | `#5DCAA5`  | `#085041` | `#0F6E56`  | Features, caching, persist   |
| coral  | `#FAECE7` | `#F0997B`  | `#712B13` | `#993C1D`  | Fusion, scratch, transforms  |
| blue   | `#E6F1FB` | `#85B7EB`  | `#0C447C` | `#185FA5`  | Compute, ViT blocks, decoder |
| amber  | `#FAEEDA` | `#EF9F27`  | `#633806` | `#854F0B`  | Text/tokenizer, warnings     |
| pink   | `#FBEAF0` | `#ED93B1`  | `#72243E` | `#993556`  | Geometry, prompts            |
| green  | `#EAF3DE` | `#97C459`  | `#27500A` | `#3B6D11`  | Segmentation, output heads   |
| red    | `#FCEBEB` | `#F09595`  | `#791F1F` | `#A32D2D`  | Errors, resets, not-impl     |
| gray   | `#F1EFE8` | `#B4B2A9`  | `#444441` | `#5F5E5A`  | Neutral, structural, generic |

#### Neutral palette

```css
--bg:     #ffffff;
--bg2:    #f7f6f3;
--bg3:    #eeedeb;
--text:   #1a1a1a;
--text2:  #6b6a65;
--text3:  #9c9a92;
--border: #e2e0d8;
```

#### Color assignment rules

- **2-3 ramps per diagram.** More = visual noise.
- **Assign by semantic category**, not by sequence.
- **Gray for neutral** elements. **Red only for warnings/errors.**
- **Stay consistent within a document.**

### Typography

```css
--sans: "Inter", "Helvetica Neue", system-ui, sans-serif;
--mono: "SF Mono", "Fira Code", "Cascadia Code", Consolas, monospace;
```

| Class        | Size    | Weight | Use                         |
|--------------|---------|--------|-----------------------------|
| page title   | 22px    | 600    | Document title              |
| `h2`         | 16px    | 600    | Major section heading       |
| `.title`     | 15px    | 600    | Subsection title            |
| `h3`         | 14px    | 600    | Component heading           |
| `.step-name` | 13px    | 600    | Step labels                 |
| `.label-md`  | 13px    | 400    | Inline subtitles (muted)    |
| body         | 12-13px | 400    | Descriptive text            |
| `.mono`      | 12px    | 400    | Code, struct fields, values |
| `.mono-sm`   | 11px    | 400    | Inline shapes, annotations  |
| `.shape`     | 11px    | 400    | Tensor shape annotations    |
| SVG text     | 9-11px  | 500-600| Diagram labels              |
| tags         | 10px    | 600    | Inline badges               |

Rules: Two weights only (400, 600). Sentence case always. No font-size below 9px (SVG) or 10px (HTML). Monospace for data, sans for everything else.

### Component Library

#### Detail box (dashed)

```css
.detail-box { border: 1.5px dashed var(--border); border-radius: 8px; padding: 12px 16px; margin-top: 8px; background: var(--bg); }
```

#### Solid box

```css
.solid-box { border: 1px solid var(--border); border-radius: 8px; padding: 12px 16px; margin-top: 8px; }
```

#### Key-value grid

```css
.kv { display: grid; grid-template-columns: auto 1fr auto; gap: 2px 12px; font-family: var(--mono); font-size: 12px; line-height: 1.8; }
.kv .k { color: var(--text2); }
.kv .v { color: var(--text); }
.kv .c { color: var(--text3); font-size: 11px; }
```

#### Inline highlights

```css
.hl       { color: var(--purple-text); font-weight: 600; }
.hl-teal  { color: var(--teal-text);   font-weight: 600; }
.hl-coral { color: var(--coral-text);  font-weight: 600; }
.hl-blue  { color: var(--blue-text);   font-weight: 600; }
.hl-amber { color: var(--amber-text);  font-weight: 600; }
.hl-pink  { color: var(--pink-text);   font-weight: 600; }
.hl-green { color: var(--green-text);  font-weight: 600; }
.hl-gray  { color: var(--text2);       font-weight: 500; }
```

#### Tags / badges

```css
.tag { display: inline-block; padding: 1px 7px; border-radius: 4px; font-size: 10px; font-weight: 600; vertical-align: middle; margin-left: 4px; }
.tag-blue { background: var(--blue-bg); color: var(--blue-text); border: 1px solid var(--blue-border); }
/* same pattern for all 9 ramps */
```

#### Pipeline flow row

```css
.flow-row   { display: flex; align-items: center; flex-wrap: wrap; gap: 6px; margin: 8px 0; }
.flow-box   { border-radius: 6px; padding: 4px 12px; font-family: var(--mono); font-size: 11px; font-weight: 600; white-space: nowrap; }
.flow-shape { font-family: var(--mono); font-size: 10px; color: var(--text3); margin-top: 1px; text-align: center; }
.pipe-arrow { color: var(--text3); font-size: 18px; margin: 0 2px; }
```

#### Numbered steps

```css
.step-header { display: flex; align-items: center; gap: 6px; margin: 16px 0 6px; }
.step-num    { width: 22px; height: 22px; border-radius: 50%; font-size: 11px; font-weight: 600; display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
.step-name   { font-size: 13px; font-weight: 600; }
```

#### Grid layouts

```css
.grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 10px; }
.grid-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 12px; margin-top: 10px; }
@media (max-width: 600px) { .grid-2, .grid-3 { grid-template-columns: 1fr; } }
```

### SVG Diagram Rules

#### Viewport

- `width="100%"` with `viewBox="0 0 W H"`.
- W = 680 (narrow) or 780 (architecture). H = content height + 20px.
- All SVG text: `font-family: var(--mono)`.

#### Boxes

- `rx="6"` module boxes, `rx="4"` small inline, `rx="10-12"` large containers.
- `stroke-width=".5"` for all box borders.
- Title: `font-size="10-11"`, `font-weight="600"`, fill = `var(--{color}-text)`.
- Subtitle: `font-size="9"`, fill = `var(--text3)`.

#### Containers

- Opacity `.5-.6` on fills so nested boxes remain visible.
- `stroke-width="1"` (slightly heavier than child boxes).

#### Arrows

- Stroke: `var(--text3)`, width `1`. Arrowhead: small triangle, 8px wide.
- Dashed for optional: `stroke-dasharray="4 3"`.
- Never route through boxes. Use L-shaped paths.

#### Leader lines

- `stroke-width=".5"`, `stroke-dasharray="3 3"`, color = `var(--border)`.

### Recurring Diagram Patterns

- **Struct docs**: Title `.mono` 600, fields in `.kv` grid, wrap in `.detail-box`.
- **Pipeline docs**: Overview `.flow-row` + arrows, then numbered `.step-header` + `.detail-box` per step.
- **Side-by-side**: `.grid-2` with two `.detail-box` or `.solid-box` cards.
- **Architecture hierarchy**: Outermost dashed container, colored groups for subsystems, module boxes inside, arrows, result box at bottom.
- **Not implemented**: Red-tagged `.flow-box` elements.

### Diagram Checklist

1. Light mode only: no `prefers-color-scheme` media queries.
2. SVG text: does every `<text>` have an explicit `fill`?
3. Box sizing: `text_width + 24px < rect_width`?
4. Arrows: does any cross an unrelated box?
5. Consistency: same components = same colors across all diagrams?
6. Mobile: collapses at 400px?
7. No gradients, shadows, blur, or decorative effects.

### Full CSS Variable Block

```css
:root {
  --bg: #ffffff; --bg2: #f7f6f3; --bg3: #eeedeb;
  --text: #1a1a1a; --text2: #6b6a65; --text3: #9c9a92;
  --border: #e2e0d8;
  --purple: #534AB7; --purple-bg: #EEEDFE; --purple-border: #AFA9EC; --purple-text: #3C3489;
  --teal: #0F6E56; --teal-bg: #E1F5EE; --teal-border: #5DCAA5; --teal-text: #085041;
  --coral: #993C1D; --coral-bg: #FAECE7; --coral-border: #F0997B; --coral-text: #712B13;
  --pink: #993556; --pink-bg: #FBEAF0; --pink-border: #ED93B1; --pink-text: #72243E;
  --blue: #185FA5; --blue-bg: #E6F1FB; --blue-border: #85B7EB; --blue-text: #0C447C;
  --amber: #854F0B; --amber-bg: #FAEEDA; --amber-border: #EF9F27; --amber-text: #633806;
  --green: #3B6D11; --green-bg: #EAF3DE; --green-border: #97C459; --green-text: #27500A;
  --red: #A32D2D; --red-bg: #FCEBEB; --red-border: #F09595; --red-text: #791F1F;
  --gray: #5F5E5A; --gray-bg: #F1EFE8; --gray-border: #B4B2A9; --gray-text: #444441;
  --mono: "SF Mono", "Fira Code", "Cascadia Code", Consolas, monospace;
  --sans: "Inter", "Helvetica Neue", system-ui, sans-serif;
}

/* No dark mode. Light mode only. */
```