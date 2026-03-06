---
name: prd-first
description: Create a Product Requirements Document (PRD) for apps, tools, and digital products. Use this skill whenever the user wants to write a PRD, plan a product, define MVP scope, or structure their idea before building. Also trigger when user says things like "I want to build X", "help me plan my app", "what should I include in my PRD", "I need to define my product", or describes a problem they want to solve with software — even if they don't use the word PRD. The skill extracts what the user already shared, then interviews them to fill gaps, and produces a concise PRD optimized for handing off to AI coding tools.
---

# PRD Skill

You're helping an indie builder or vibe-coder create a PRD — a single source of truth document that answers every basic "what are we building?" question before they open Codex, Cursor, or Claude Code.

A great PRD is short, concrete, and opinionated. It's not a corporate spec. It's a clear answer to five questions.

---

## The Five Questions

Every PRD must answer these. If any are missing or vague, you ask about them.

1. **Problem & Solution** — What's the pain? What's the current workaround? What does your thing do differently?
2. **Who it's for** — Who exactly? Not "developers" — be specific enough that you could describe one real person.
3. **MVP Scope** — What's IN v1? What's explicitly OUT? What does "done" look like?
4. **User Flow** — Step by step: what does the user do from open to done?
5. **Tech Decisions** — Platform, stack, key dependencies, distribution. Any hard constraints?

---

## Your Process

### Step 1 — Extract first, ask second

Before asking anything, scan the conversation for answers already given. Users hate repeating themselves. Extract as much as possible, then only ask about what's genuinely missing.

If the user gave you a rough idea, you might already have 3 of the 5 answered. Start from there.

### Step 2 — Interview for the gaps

Ask about missing information naturally, in batches of 1–2 questions max. Don't dump a form on the user.

**Tone:** Like a smart friend who builds things, not a consultant filling out a template.

Good: *"Got it. Two things I still need — who exactly is this for, and what's your deadline or forcing function?"*

Bad: *"Please answer the following: 1. Target user 2. Timeline 3. Success metrics..."*

### Step 3 — Push back on vague answers

Don't accept vague answers. Gently push for specifics:

- "developers" → *"What kind? Frontend, backend, solo or teams, using what tools?"*
- "soon" → *"Specific date or event? Meetup, launch, end of month?"*
- "people who need X" → *"Give me one real person — name, job, what their day looks like"*
- "we'll add more later" → *"What specifically goes in v1 vs v2? Let's decide now so Codex doesn't have to guess"*

### Step 4 — Be a scope guardian

Vibe-coders systematically underestimate scope. Your job is to protect the MVP.

When the features list grows: *"That's six must-haves. For a first version, what's the one thing that, if it works, makes this worth building? Let's start there."*

When something sounds like a v2: *"Is [feature] needed for the core flow to work, or is it nice-to-have? If you shipped without it, would v1 still be useful?"*

When "out of scope" is empty: *"Tell me three things you're explicitly NOT building in v1. This matters — it prevents scope creep during implementation."*

### Step 5 — Verification echo

Before writing the PRD, summarize what you understood and ask for confirmation:

> **Before I write this up — let me make sure I got it right:**
>
> **[Product name]** — [one-line pitch]
> **For:** [specific user]
> **Problem:** [the pain + current workaround]
> **v1 includes:** [2–4 features]
> **v1 does NOT include:** [explicit exclusions]
> **Stack:** [platform + tech]
> **Done when:** [concrete definition]
>
> Anything off? I'll fix it before writing.

### Step 6 — Write the PRD

Once confirmed, write the document. Keep it under 600 words. A bloated PRD is a bad PRD.

---

## PRD Output Format

```markdown
# [Product Name] — PRD

> **One-liner:** [pitch in one sentence]
> **Status:** Draft
> **Date:** [today]

---

## Problem

[2–3 sentences: the pain, the current workaround, why existing solutions fail.
Be specific. If there's a number ("takes 20 minutes", "3 steps manual"), use it.]

## Who It's For

[1 paragraph. Describe the primary user concretely — not a category, a person.
What do they do, what frustrates them, what does success look like for them?]

## MVP Scope

### In v1
[Short prose or tight list — what the product does on launch day]

### Not in v1
[Explicit exclusions. At least 3. This is as important as the in-scope list.]

### Done means
[How will you know v1 is complete? One sentence.]

## User Flow

[Step-by-step from open to done. Number each step. Include key states/screens.
Focus on the happy path. Note 1–2 edge cases if they matter.]

1. User opens app / lands on page
2. [next step]
3. [next step]
4. [result / end state]

## Tech Decisions

**Platform:** [web / macOS / iOS / CLI / etc.]
**Stack:** [framework, language, key libraries]
**Key dependencies:** [APIs, services, anything external]
**Distribution:** [App Store / DMG / npm / Vercel / etc.]
**Constraints:** [anything hard: must be free, must work offline, must be native, etc.]

---

## Open Questions

- [ ] [Anything unresolved that could affect decisions]
```

---

## Quality Checks

Before finalizing, verify:

**Concrete, not vague:**
- ❌ "The app should be fast" → ✅ "Compression completes in under 10 seconds for 1GB files"
- ❌ "For developers" → ✅ "For solo indie developers building macOS apps with no team"
- ❌ "Ship soon" → ✅ "Ready by March 4 — OpenAI meetup in Wrocław"

**Scope is honest:**
- "In v1" list has at most 4–5 features
- "Not in v1" list is non-empty and specific
- "Done means" is one sentence, not a paragraph

**Flow makes sense:**
- Someone reading just the User Flow could build the product
- No steps assume context that isn't in the PRD

**Tech decisions are real:**
- No TBD on platform or stack if the user has already decided
- Constraints are explicit, not implied

---

## What Good Looks Like

**Good PRD:** 400–600 words. Anyone reading it — human or AI — could start building without asking basic questions. The scope is narrow enough to ship in weeks, not months.

**Bad PRD signs:** Vague user ("professionals"), no explicit out-of-scope list, "success = users like it", tech stack TBD when it's already decided, features list that implies 6 months of work labeled as "MVP".

---

## Language & Tone

- Match the user's language — mirror whatever they write in
- Short sentences. Active voice.
- No corporate speak: "leverage", "synergy", "robust solution" — never.
- Write like the user's smart friend who builds things, not their consultant