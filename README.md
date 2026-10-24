# Brain Summarize Conversation

> **Tri-Platform Agent Skill** for Claude Desktop / Code, Grok CLI, and Google Antigravity / Gemini.  
> Executive Brief Condensation into Second Brain — Condenses active conversation into a structured executive brief (Objective, Accomplishments, Decisions, Next Steps) and saves directly to Second Brain.

---

## Overview

`brain-summarize-conversation` provides standardized capabilities across conversational AI platforms:
- 4-part executive brief extraction (Objectives, Accomplishments, Decisions, Next Steps).
- Automated extraction of key conventions and architectural choices.
- Direct persistence to Second Brain with #summary and !state flags.
- Tri-platform NTFS junctions connecting Claude, Grok, and Antigravity.
- Standard documentation suite: SKILL.md, HOW_TO_USE.txt, IMPLEMENTATION_PLAN.md, and README.md.

---

## Tri-Platform Architecture

Zero duplicate code across platforms. Canonical source resides in `.agents`:
- **Canonical Source**: `C:\Users\<you>\.agents\skills\brain-summarize-conversation`
- **Claude**: `C:\Users\<you>\.claude\skills\brain-summarize-conversation` (NTFS Junction)
- **Grok**: `C:\Users\<you>\.grok\skills\brain-summarize-conversation` (NTFS Junction)
- **Antigravity**: `C:\Users\<you>\.gemini\config\skills\brain-summarize-conversation` (NTFS Junction)

---

## Documentation Suite

- [`HOW_TO_USE.txt`](HOW_TO_USE.txt): Standardized user guide and prompt templates.
- [`IMPLEMENTATION_PLAN.md`](IMPLEMENTATION_PLAN.md): Feature checklist and roadmap.
- [`App Changes Tracker.html`](App%20Changes%20Tracker.html): Interactive visual version log.
- [`SKILL.md`](SKILL.md): Agent system instructions and triggers.
