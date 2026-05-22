# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is a **single-deliverable specification project**, not a software codebase. It contains one source document — `AquaGuard_BMC_Prompt_for_ClaudeCode.md` — which is a detailed spec/prompt that drives generation of **one output file: `AquaGuard_BMC.html`**.

There is no build system, package manager, test suite, or dependencies to install. The "workflow" is: read the spec completely, then produce the HTML file. Validate by opening the generated `.html` in a browser and using the browser's print preview (the document is print-targeted).

## The deliverable: `AquaGuard_BMC.html`

A professional, print-ready Business Model Canvas for **AquaGuard** — a mobile-based emergency rescue support system for flood disasters (HCMUT student project). The Business Model Canvas is the *product being documented*; AquaGuard's actual software stack (iOS SwiftUI app, React web dashboard, Node.js backend) lives elsewhere and is not in this repo.

### Hard constraints (do not violate)

- **One self-contained file.** All CSS in an inline `<style>` tag, all JS in an inline `<script>` tag.
- **Only external dependency allowed: Google Fonts** (DM Sans for headings, Inter for body).
- **Reproduce spec content exactly.** Every BMC bullet, roadmap item, and table cell in the spec must appear verbatim — do not simplify, summarize, paraphrase, or omit. This includes Vietnamese names/diacritics (e.g., Thiền viện Vạn Hạnh, Quỹ Đất Lành, Võ Thanh Hằng) and `[NEW]` / `[PRIMARY]` badges.

## Architecture of the generated HTML

The page is organized as six top-level sections in order: Header → Phase Navigation Tabs → BMC 9-block Grid → Roadmap → Delta Comparison Table → Footer.

Two structural ideas drive the implementation:

1. **Three phases, all pre-rendered, toggled by JS.** The BMC content exists for Phase 1 (MVP & Research), Phase 2 (Full Deployment), and Phase 3 (AI + Drone). All three are rendered into the HTML; tab clicks switch visibility via `display` none/block with a ~0.2s opacity fade. The Roadmap and Delta table are *always visible* regardless of active tab.

2. **The 9-block BMC is a 10-column CSS Grid.** Blocks are placed with explicit `grid-column` / `grid-row` spans (Value Propositions and Customer Segments span two rows; Cost Structure and Revenue Streams form a 5-col bottom row). The exact grid placement is specified in the source doc — follow it.

### Print support is a first-class requirement

`@media print` must hide the tab navigation, force *all three* BMC phases to display (overriding the JS toggle), and insert page breaks before the Roadmap and Delta sections. The whole document must read correctly as a printed/PDF artifact, not just on screen.

### Design tokens

The spec defines the exact palette (navy `#1B2A4A`, teal `#1D9E75`, plus per-block accent colors), typography scale, `[NEW]` badge styling (Phase 1/2 green, Phase 3 purple), and 1100px max centered width. Use these literal values — they are an intentional, fixed design system, not suggestions.

### Responsive behavior

Desktop = full 10-column grid; tablet (`< ~768px` region) = simplified 2-column; mobile = single stacked column.

## Working in this repo

When asked to (re)generate or modify the deliverable, **read `AquaGuard_BMC_Prompt_for_ClaudeCode.md` in full first** — it is the single source of truth for content, layout, colors, and the page section order. The bottom of that document contains the canonical generation instructions.
