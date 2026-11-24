# MikeGC legal core (reference extract)

The legal-specific parts of [MikeGC](https://github.com/open-legal-products/mikegc),
itself a fork of [Mike (MikeOSS)](https://mikeoss.com), extracted for reading and study.

**This is not a runnable project.** The files import shared infrastructure
(`backend/src/lib/*`, database, queue, auth) that is not included. For the full
application, use the upstream repository.

## What is here

| Path | What it does |
| --- | --- |
| `backend/src/modules/playbooks/` | Compiles a Word/PDF negotiation guide into structured rules and reviews contracts against them (statuses, quotes, suggested redlines, tracked changes). |
| `backend/src/modules/intake/` | Legal-team request tracker plus the LLM agent that triages Gmail, Outlook, Slack and Teams threads. |
| `backend/src/modules/tabular/` | Documents-by-columns review grid with typed, cited extraction. |
| `backend/src/modules/quick-actions/` | One-click assistant actions. |
| `backend/src/modules/chat/engine/` | Legal assistant system prompt, tool dispatch, citation parsing and verification, Word edits. |
| `backend/src/lib/courtlistener.ts` | US case-law lookup and citation verification via CourtListener. |
| `backend/src/lib/docxTrackedChanges.ts` | Applying suggestions to .docx as tracked changes. |
| `packages/contracts/` | Shared API/event types. |
| `docs/` | Feature documentation for the above. |

## Licence and attribution

Upstream is licensed AGPL-3.0-only. This extract keeps that licence (`LICENSE`)
and the upstream `CREDITS.md`. Anything built from it must comply with the AGPL.
Not legal advice; the model output these prompts produce needs lawyer review.
