# Prometheus Aminos — Hero Lab

Design playground for the **home page hero** of Prometheus Aminos, built on the line **"Stolen from the Gods."**

Everything here is plain HTML, CSS and vanilla JavaScript. There is no build step and nothing to install. Open a file in a browser and it runs.

**Live preview (GitHub Pages):** https://andrewgoodson.github.io/prometheus-aminos-hero-lab/

## What's inside

| Path | What it is |
|---|---|
| [`index.html`](index.html) | **Current round.** Seven animated, mouse-reactive heroes in which our torch-and-pillar mark feeds an amino-acid chain. Black, gold, four moods. |
| [`concepts/god-torch-chain.html`](concepts/god-torch-chain.html) | A god in gold outline raises the torch; its flame drains into a peptide chain. |
| [`concepts/first-four-directions.html`](concepts/first-four-directions.html) | First round: The Theft, Olympus to Earth, The Vase, Marble and Fire. Also the heading-font comparison. |
| [`concepts/hand-to-hand.html`](concepts/hand-to-hand.html) | Rejected round (reads as "ping pong"); kept for reference only. |
| [`BRIEF.md`](BRIEF.md) | **Start here if you are an AI.** The design brief, the owner's answers, and what "better" means. |
| [`BRAND.md`](BRAND.md) | Brand rules: name, logo, colour, type, voice, and the wording that is never allowed. |
| [`brand/tokens.css`](brand/tokens.css) | Colour and type tokens as CSS custom properties. |
| [`brand/logos/`](brand/logos) | Official mark, wordmark and lockup (SVG and PNG). |

## Using this with Grok (or any AI)

Give it the repo URL and a prompt like:

> Read `BRIEF.md` and `BRAND.md` in https://github.com/AndrewGoodson/prometheus-aminos-hero-lab, then study `index.html`. Make Hero 2 (Molecule in the Fire) better: [your idea]. Return one complete, self-contained HTML file in the same style as `index.html`. It must follow every rule in BRAND.md, especially the forbidden wording.

Good things to ask for:
- "Combine Hero 2's molecule with Hero 4's centred luxury layout."
- "Give me three new chain styles that are not beads."
- "Make the flame-to-chain hand-off feel like the fire is being stolen."
- "Make it feel more like a museum piece / a product launch / a precision instrument."

Save what it returns as a new file in `concepts/` (for example `concepts/grok-01-molecule-luxury.html`) so every idea stays side by side.

## How a chosen hero gets onto the real site

The live store is a WordPress theme with no framework, so the winning hero has to stay **one HTML block + one CSS block + one vanilla JS file**: no React, no build tools, no external libraries, under about 30 KB of JS. It must also respect `prefers-reduced-motion`, work at 390 px wide, and keep the headline as real text. BRIEF.md lists the full set of rules.

## Rights

The Prometheus Aminos name, flame mark, wordmark and lockup are the property of Prometheus Aminos and are **not** licensed for reuse. They are shared here only so the hero can be designed. Fonts load from Google Fonts (EB Garamond, Montserrat; SIL Open Font License).
