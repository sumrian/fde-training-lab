# ChatGPT Project / Work Migration

## Goal

GitHub is the long-term canonical source.

ChatGPT Project is the persistent training workspace.

Each new simulation should preferably be a separate Chat or Work thread inside the same Project.

## Step 1 — Create Project

Create a ChatGPT Project named:

> FDE Training Lab

## Step 2 — Move Current Conversation

Move the current long conversation into the Project.

This preserves the full evolution:

- original real FDE problem
- initial lessons
- FDE preflight playbook
- Case 001 simulation
- Case 001 review
- project design discussion

## Step 3 — Add Project Instructions

Copy the content of:

`prompts/project-instructions.md`

into Project Instructions.

## Step 4 — Add Core Files

Upload or add at least:

- `framework/scoring-rubric.md`
- `framework/competency-model.md`
- `framework/simulation-protocol.md`
- `progress/current-profile.md`
- `playbook/fde-preflight.md`

Optional:

- whole repository archive
- Case 001 review
- score history

## Step 5 — Start New Work

Inside the Project, start a new Work chat for each major simulation.

Naming convention:

- Case 002 — Scope Pressure
- Case 003 — Low Cooperation
- Case 004 — Executive Pressure

Do not put all future simulations into one endless thread.

## Step 6 — End-of-case Sync

After each review, update GitHub canonical files:

- simulation case
- review
- score.yaml
- current-profile
- score-history
- recurring-patterns
- playbook when a lesson is reusable

## Operating Model

### GitHub

Stores:

- canonical rubric
- playbook
- case archive
- scores
- current skill profile
- reusable prompts

### ChatGPT Project / Work

Used for:

- live role play
- dynamic challenge
- long-form reasoning
- post-case discussion
- iteration

The workflow is:

> Work → Review → Distill → GitHub → Next Work
