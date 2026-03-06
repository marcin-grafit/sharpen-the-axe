# Sharpen the Axe First 🪓

> Skills and resources from the talk *"Sharpen the axe first: think before you vibe"*
> OpenAI Community Meetup — Wrocław, March 2026

---

## The idea

Vibe-coding works. But most people skip the prep and go straight to prompting — and then spend hours fixing what the AI got wrong because it didn't have enough context.

The talk covered a 3-step workflow that runs before you open Codex, Cursor, or Claude Code:

```
1. Write a PRD        →  what you're building and what you're not
2. Write a Design System  →  tokens, components, visual language
3. Generate a Master Prompt  →  one file that briefs the AI agent completely
```

The AI coding session only starts at step 4. Everything before that is the axe-sharpening.

---

## What's in this repo

### Skills

Each skill comes in two formats. Use whichever fits your tool:

| Skill | Claude Projects | Codex / Cursor / Claude Code | What it does |
|---|---|---|---|
| PRD | [`prd-first.skill`](./prd-first.skill) | [`prd-first.md`](./prd-first.md) | Interviews you and writes a tight PRD optimized for AI coding tools |
| Master Prompt | [`master-prompt.skill`](./master-prompt.skill) | [`master-prompt.md`](./master-prompt.md) | Takes your PRD + Design System and generates a complete agent briefing |

`.skill` files are for Claude Projects (drag and drop into your project). `.md` files are plain markdown you can use with any AI coding tool.

### Useful links

Resources mentioned in the talk:

| Resource | What it's for |
|---|---|
| [Shadcn UI](https://ui.shadcn.com) | Component library — good reference for design systems |
| [Spotted in Prod](https://spottedinprod.com) | Real UI patterns from production apps |
| [Refero](https://refero.design) | Design references from top products |
| [Mobbin](https://mobbin.com) | Mobile and web UI pattern library |
| [Free Faces](https://freefaces.gallery) | Curated free fonts |
| [Randoma11y](https://randoma11y.com) | Accessible color pair generator |

---

## How to use the skills

Skills are plain text instruction files. You give them to an AI agent alongside your other files — the agent reads them and knows what to do.

### Step 1 — Write your PRD

Upload `prd-first.md` (or `.skill` for Claude) together with a short description of your idea. Say:

> *"Use the prd-first skill to write a PRD for my app"*

Codex will interview you and produce a ready PRD.

### Step 2 — Prepare your Design System

Pull your tokens from Figma or write them by hand. Keep it in a single file — `DesignSystem.swift`, `tokens.ts`, whatever fits your stack.

### Step 3 — Generate the Master Prompt

Upload `master-prompt.md` (or `.skill` for Claude) + your PRD + your Design System to Codex. Say:

> *"Use the master-prompt skill to write a master prompt for my app"*

Codex will identify gaps, ask about them, and generate one complete briefing file.

### Step 4 — Build

Upload to Codex:
- `master-prompt.md`
- `DesignSystem.swift` (or equivalent)
- Screenshots of designed screens (Codex can't open Figma URLs)

One prompt:

> *"Implement the app based on these files."*

Codex reads the master prompt once and builds autonomously.

---

## About

Built by [Marcin Warno](https://linkedin.com/in/marcinwarno) / [GRAFIT](https://grafit.io)