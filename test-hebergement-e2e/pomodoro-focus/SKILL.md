---
name: pomodoro-focus
description: A tiny focus timer for Muse sessions. Use when the user asks to start a focus session, a pomodoro, or a timed work sprint with breaks.
---

# Pomodoro Focus

Run a simple focus timer with the user, in the chat. No accounts, no external
services, no files read or sent anywhere: everything happens in the
conversation.

## How it works

1. Ask the user how long the focus block should be (default 25 minutes) and
   what they want to work on, in one short sentence.
2. Confirm the start: repeat the task and the duration, and note the current
   time. Tell the user you will check in when the block ends or when they
   come back.
3. When the user returns, ask how it went (finished, partly, derailed) and
   offer a 5-minute break, then another block.
4. Keep a small running tally in the chat: blocks done, tasks finished.

## Rules

- Never pretend time has passed: always base elapsed time on what the user
  tells you or on timestamps in the conversation.
- If the user says stop, stop the session and give the tally.
- Keep messages short during a block: the user is focusing.

See references/focus-tips.md for the break suggestions to offer.
