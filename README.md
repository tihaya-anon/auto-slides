# Slides Framework

This directory contains a minimal Quarto stack for quant course material.

## Outputs

- `slides/video-lesson.qmd`: reveal.js slides for recording or autoplay
- `handouts/web-notes.qmd`: HTML handout for web publishing
- `handouts/pdf-notes.qmd`: PDF handout for printing or offline reading

## Why This Structure

The video deck and the reading material should not be the same artifact.

- slides favor timing, motion, sparse text, and narration
- handouts favor detail, derivations, and review

Quarto lets you keep those outputs in one project without forcing you back into a full Beamer workflow.

## Render Commands

```bash
quarto render slides/video-lesson.qmd
quarto render handouts/web-notes.qmd
quarto render handouts/pdf-notes.qmd
quarto render
```

## Suggested Lecture Pattern

1. Put the core story into `slides/video-lesson.qmd`.
2. Keep narration in `::: {.notes}` blocks.
3. Generate TTS from notes and align it with slide timing.
4. Put extra derivations, assumptions, and figures into the handouts.
5. Publish `_site/` to GitHub Pages and export PDF when needed.

## TTS / Video Notes

The deck already demonstrates the key pieces:

- reveal.js `auto-slide` for automatic pacing
- speaker notes as a clean source for narration text
- formula, code, and figure layout for quant topics

In practice you will likely want to set `auto-slide` per slide once your narration timings are stable.
