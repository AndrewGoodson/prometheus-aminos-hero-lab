# Hero brief

## The business, in one paragraph

Prometheus Aminos sells research peptides (short amino-acid chains) **for in-vitro laboratory research only**, to buyers aged 21 and over. Every batch is tested by an independent third-party lab; each order ships with a QR code that opens that batch's result on the testing lab's own website. The store is calm, exact and classical: a laboratory supplier, not a supplement brand.

## The job of the hero

The first screen of the home page. In two seconds a visitor should feel: *this is serious, premium, scientific, and has a myth behind it*, then click **Shop** or **Lab Results**.

## The idea

In Greek myth, Prometheus stole fire from the gods and gave it to people as knowledge: the start of craft and science. Our mark is his torch: a flame on a fluted pillar. The hero shows **that fire becoming an amino-acid chain**, the thing we sell.

## Owner's answers (fixed for this round)

| Question | Answer |
|---|---|
| Headline | **Stolen from the Gods.** (nothing else in the headline) |
| Supporting line | Research compounds, sold by size. Every batch tested by an independent lab. |
| Buttons | **Shop** (solid) + **Lab Results** (outline) |
| Background | **Black** |
| Colour | **Gold only** for flame and chain (amber highlights allowed), ivory text |
| Torch and pillar | Our mark stands on its own and **its flame feeds the chain** |
| Chain style | Ball-and-stick 3D, chemistry line drawing, or particle stream. **No plain beads.** |
| Interaction | **Plays on its own** and **leans/reacts to the mouse** |
| Motion | **Medium**: visible flicker, sparks travel, chain sways. Never distracts from the headline. |
| Phones | Same hero, smaller, fewer particles |
| Mood | Explore all four: museum/classical, precision lab, luxury, product launch |

The owner has liked: the black option with a glowing torch, and the idea of the flame draining into a chain. The owner has rejected: a spark bouncing between two hands ("ping pong"), cartoon beads, and anything that looks like a template shop.

## What "better" means

1. The fire visibly **becomes** the chain. A clear hand-off from flame to molecule, not two things side by side.
2. The chain reads as a **peptide** (one twisting backbone, N–C–C(=O) repeating, side groups), **not DNA** (no two-strand ladder).
3. It feels expensive: restraint, depth, light that behaves like light.
4. The headline stays the hero. The art supports it and never sits behind the text where it hurts contrast.
5. Smooth: 60 fps on a laptop, no jank on a mid-range phone.

## Hard rules (the work is rejected if any are broken)

- **No body, no person absorbing the fire, no "getting stronger".** Fire goes to the torch, the chain or the lab. Showing power entering a human reads as a health or performance claim, and this store cannot make one.
- No syringes, pills, muscles, skin, medical or clinical props.
- No wording from the forbidden list in BRAND.md. Do not add new marketing copy; use the headline, line and buttons above.
- Do not redraw or retype the PROMETHEUS wordmark. The torch mark may be tinted gold and animated in the hero only.
- Text contrast at least 4.5:1 (ivory on black is fine).
- `prefers-reduced-motion: reduce` gives a still, finished-looking frame.
- Canvas and SVG art are decorative: `aria-hidden="true"`. Headline and buttons are real text and real links.

## Technical rules (so it can go on the real site)

- One self-contained HTML file per concept: inline `<style>`, inline vanilla `<script>`. Google Fonts link is fine.
- **No frameworks, no libraries, no build step**, no WebGL libraries (raw Canvas 2D or raw WebGL is fine). Keep JS under about 30 KB.
- Pause animation when the hero is off screen (IntersectionObserver), cap devicePixelRatio at 2.
- Works from 360 px to 2560 px wide. On phones the art sits above the headline.
- Brand tokens in `brand/tokens.css`; reuse them.

## How index.html is built (to extend it)

Each `.hero` has `data-kind` (`helix`, `model`, `formula`, `thread`) and optional flags (`data-rise`, `data-cinema`, `data-museum`, `data-instrument`). A small `Hero` class creates the canvas, clones the torch SVG from `<template id="torchTpl">`, tracks an eased mouse position, and calls `R[kind](hero, ctx, timeSeconds)` every frame. `hero.src` is the flame tip in canvas pixels, so the chain always starts at the fire. Add a new look by writing a new `R.yourKind` function and a new `.hero` block.
