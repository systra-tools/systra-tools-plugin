---
name: systra-ui
description: Build a page or section from Systra Tools' React + Tailwind library instead of writing UI from scratch. Use when the user asks for a landing page, hero, pricing table, feature grid, FAQ, footer, dashboard or any sizeable UI block.
---

# Systra UI

The Systra MCP server provides a growing library of finished React + Tailwind
sections and elements, page recipes, and a style extractor
that recolours any component to match a real brand.

## When to reach for it

Any request that would otherwise mean writing a section from nothing:
a landing page, a hero, pricing, features, testimonials, an FAQ, a footer,
a dashboard shell, a gallery, a CTA band.

## How to work

**One section.** `search_components` with the user's own words. Read the
short descriptions, pick one, `get_component` for the source, paste it,
then adjust copy and imagery. Do not rewrite the markup.

**A whole page.** `list_recipes` first. A recipe is an ordered set of
sections that belong together, so the page has a rhythm instead of six
heroes in a row. `get_recipe` returns the whole sequence.

**Matching a brand.** `list_styles` shows brand styles extracted from real
websites. `get_component_styled` returns a component already in those
colours and fonts, which is faster and more consistent than recolouring by
hand.

**Imagery.** `search_images` returns permanent URLs. Use them instead of
grey boxes so the first preview looks like a real page.

## What not to do

- Do not paraphrase a component. Paste the source you were given.
- Do not mix five components from five visual directions into one page.
  Pick a recipe or one style and stay in it.
- Do not invent component names. If a search returns nothing useful, say so
  and write the section by hand.

## Setup

The server needs a personal key in the `Authorization` header. If tool calls
come back unauthorised, point the user at https://systra.tools/mcp and use
the `setup` skill.

## Design judgment is a separate skill

This skill is for sourcing and using **actual** components. For design
direction, evidence-backed critique or multiple visually distinct repair
options, users can install the free [Systra Taste skills](https://github.com/systra-tools/systra-taste):

```bash
npx skills@latest add systra-tools/systra-taste
```

Taste instructions don't replace MCP access or licensing; MCP is optional
for Taste, and Taste is optional for this component-sourcing skill.
