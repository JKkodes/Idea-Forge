# Idea-Forge
**Turn a vague idea into a tested decision — before you build it.**
IdeaForge is a conversational AI tool that helps you stress-test an idea before you commit real time to it. Instead of jumping straight from "I have an idea" to "let me start building," it walks you through clarifying the idea, surfacing the assumptions it depends on, mapping out the risks, and comparing it against common patterns of what tends to work and what tends to fail — then puts the final call in your hands.

## Why it exists

Most people — students, first-time founders, anyone with a new idea — start building or committing time before checking whether the idea actually holds up. By the time something breaks, the time's already spent. IdeaForge exists to catch that earlier, in minutes instead of weeks.

## Features

- **Conversational idea clarification** — answers targeted questions about your user, the real problem, and why this even needs AI
- **Assumption surfacing** — names the things you're quietly betting on
- **Risk mapping** — what happens if those assumptions are wrong, with mitigations
- **Reference profile** — compares your idea against common success and failure patterns for that category
- **Human-locked decision gate** — you explicitly choose BUILD, PIVOT, or DROP; the AI never decides this for you
- **30/60/90-day execution plan** — generated only after you commit to building, ending in one concrete first step
- **Challenge My Idea** — a second AI pass that stress-tests your own plan to find its single weakest, least-validated assumption

## How it works

1. **Idea Capture** — describe your idea in plain language
2. **Clarification** — the system asks what it actually needs to know
3. **Assumption Surfacing** — what has to be true for this to work
4. **Risk Analysis** — what breaks if it isn't
5. **Reference Profile** — how this compares to known patterns
6. **Decision Gate** — you choose: BUILD / PIVOT / DROP
7. **Execution Plan** — a real 30/60/90-day roadmap, only on BUILD
8. **Challenge My Idea** — a second pass that finds the plan's weakest link

## Getting started

IdeaForge is a single HTML file — no build step, no installation, no backend.

1. Download `index.html`
2. Open it in any modern browser
3. On first launch, you'll be asked for a free Gemini API key — get one in under a minute at [aistudio.google.com/apikey](https://aistudio.google.com/apikey)
4. Your key is stored only in your browser's local storage and is sent only to Google's API — never anywhere else

## Tech stack

- HTML / CSS / vanilla JavaScript — no framework, no build tooling
- [Google Gemini API](https://ai.google.dev/) (`gemini-2.5-flash`) for all reasoning

## Design notes

**Why a single file, no backend?** Simplicity and portability it runs anywhere, instantly, with nothing to install. Because there's no backend to hold a secret server-side, the app asks for your own API key at runtime instead of shipping one meaning the source stays fully public and inspectable with nothing sensitive in it.

**Why does the AI ask before deciding?** The core design principle behind IdeaForge: it reasons, you decide. At every stage where the system could just hand you an answer, it instead hands you the reasoning and waits for your call including a hard decision gate before any plan is generated, and honest signals (like flagging high market risk) even after you've already committed to building.
