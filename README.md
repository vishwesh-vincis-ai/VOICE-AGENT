# Voice Agent (Project 1)

Autonomous call operations: inbound answering and booking, outbound reminders, no-show recovery, re-engagement.

Status: **not started**. Build order: brain → lead engine → **voice agent** → hybrid agent.

## What it does
- Inbound: answer, check live availability, book / reschedule / cancel, WhatsApp confirmation with location pin.
- Outbound: reminders, no-show recovery, re-engagement.
- After every call: intent, outcome, sentiment, follow-ups → structured data.
- Low confidence → warm transfer to a human with a summary.
- QA agent scores every call against a rubric.

## Depends on Business Brain
`POST /chat` (answers + handoff), `GET /calendar/slots`, `POST /calendar/book|reschedule|cancel`.

## Stack
LiveKit Agents or VAPI, Deepgram STT, fast LLM for live turns, Langfuse tracing.
Hard target: **response start under ~1 s, measured per turn.**
