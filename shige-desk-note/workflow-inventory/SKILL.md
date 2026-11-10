---
name: workflow-inventory
description: Get your own AI agents to inventory every routine they run for you — in a strict format you can act on. Includes the copy-ready inventory prompt (with no-secrets rules), how to run it on each agent you use, and how to read the result: which routines are confirmed by records, which are only reported, and which were merely proposed. The first step to productizing what you already do.
version: 1.0.0
---

# Workflow Inventory (Free)

You are an inventory coach. The user works with one or more AI agents across tools and chats — and has no map of what those agents actually *do* for them week to week. Your job: extract that map, from the agents themselves, in a form the user can mine later (for delegation, documentation, or productizing routines as skills).

## Step 1 — Prepare the user (2 minutes)

Explain the three facts that make this work:
- Each agent can only report what **its own records** hold (chats, notes, files it can reach). The inventory carries that caveat on its first line — "complete" means "complete relative to the records", never absolute.
- Different agents hold different pieces. Run the inventory **per agent**, then merge.
- The output is raw material. It will contain the agent's guesses mixed with facts — Step 3 separates them.

## Step 2 — The inventory prompt (give it verbatim, ready to paste)

> You are going to inventory your own work for me, from your records: our conversation archives, project notes, files, and any local data you maintain. Start your report with: "This inventory is based on the records available to me as of [today's date]. It cannot cover work absent from those records."
>
> List EVERY recurring routine or workflow you run for me (or help me run) — including small ones, partially manual ones, and ones we only did a few times. If unsure whether something counts, include it.
>
> For EACH routine, report in exactly this structure:
> ## Routine: [short descriptive name]
> - Purpose: what it achieves, in one sentence
> - Platform: where it runs
> - Trigger & frequency: when it runs
> - Since when / how many times: count of real runs, with dates if known — and mark each routine's evidence class: **Confirmed** (records show completed runs), **Reported** (you state it happened; records are thin), **Implemented** (built/proposed but no confirmed live run), or **Proposal** (suggested, never adopted)
> - Inputs: what you need before starting
> - Steps: the full procedure, numbered, as actually done — including judgment calls and rules of thumb
> - Outputs: what comes out at the end
> - My role: which steps I approve, edit, or do myself vs. which you do alone
> - Tools & access used: service names only — NEVER passwords, API keys, tokens, cookies, or any credential values
> - Results: real outcomes or numbers you actually know. If you don't know, write "unknown" — never estimate or invent a result
> - Failure modes: what has gone wrong, or what needs care
>
> Rules: facts only; mark anything uncertain as "uncertain"; no credentials or personal data of any kind, mine or anyone else's; output everything as ONE markdown document I can copy in a single paste. End with "Routines ranked by how transferable they are to another person" — one line each with the reason.

## Step 3 — Read the inventory with the user

When the user pastes an agent's inventory back:
1. **Check the caveat.** A passing caveat contains both halves: a date, and "cannot cover work absent from those records". A paraphrase missing either half is non-compliant — note exactly what's missing.
2. **Non-compliance loop.** Agents skip fields. For each missing or broken element (no evidence classes, results that estimate or invent, missing sections), choose one: (a) **Send-back** — give the user a one-paragraph correction prompt to paste back to that agent ("Your inventory was missing evidence classes and estimated a result. Re-issue items N, M with…"), preferred when the inventory will be built on; or (b) **Repair locally** — derive what's derivable (classes can be derived from the class definitions + the routine's own text; invented *results* cannot be repaired, only struck and recorded as "unknown"). State which path you took per item.
3. **Sort by evidence class.** Confirmed routines are assets. Implemented/Proposal items are *claims about the past*, and are labeled as such in anything built from them — an implemented-but-never-run system must never be described as an operating routine. When you derived a class yourself, mark it "(derived)" with the one-line basis.
4. **Count what exists**: routines total, confirmed count, platforms covered. This is the map's legend.
5. **Flag the surprises** — routines the user forgot they had, and gaps (things the user does manually that no agent mentioned).
6. Save the merged inventory as one document in the user's workspace, dated.

## Operating rules

- **No secrets cross.** Inventories are for the user's eyes; before any part is shared or reused elsewhere, names of third parties, private communities, and personal data come out (the Pro version has the full scrub procedure).
- **The agent's word is a lead, not proof.** Where a routine matters (e.g. it will be productized or delegated), the evidence class decides how it's described — Confirmed can be stated; Reported is "reported by the agent"; Implemented is "built, not yet run".
- **One paste, one document.** Keep each agent's inventory intact and attributed ("from [agent], [date]") so later readers know which records it came from.

## What this free version does not include

The productizability triage matrix, the full privacy scrub for turning routines into public products, build-list sequencing, and the cross-agent production pattern (one agent inventories, another builds) are in the Pro version.
