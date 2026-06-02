# Lesson 2 — API Endpoints · Spec-Driven Build (SDD)

The **build-it-yourself** companion to Lesson 2. Instead of reading the finished
exercise, you rebuild the lab's culminating script — `06-prompt-template.py` —
from a short spec, driving a coding agent (Claude Code) with `PROMPT.md`. Then
you score your build against the reference using the bundled `validate-lab`
skill.

You've already studied the worked lab in the main Lesson 2 repo; this is where
you practice *producing* it from a spec.

## Get the lab

This is its **own repo** — clone it fresh and work inside it (the answer key is
deliberately *not* here, so your agent starts from a clean slate):

```bash
git clone https://github.com/ProciGen-AI/lesson-02-api-endpoints-sdd.git
cd lesson-02-api-endpoints-sdd
```

## Set up

> **On Windows?** Run these from **Git Bash** (easiest via VS Code's integrated
> terminal) — PowerShell can't source a `.sh` file.

```bash
source setup.sh                  # creates/activates the shared venv, installs deps, Bedrock smoke test
cp .env.example .env             # then fill in AWS creds + BEDROCK_MODEL_ID (.env.example documents each var)
mv CLAUDE.md-example CLAUDE.md   # activate the build conventions your agent reads
```

## Build

Open this folder in your coding agent and hand it `PROMPT.md`. It's a *partial*
spec — the load-bearing design decisions are left to you (see the `▢ YOU DECIDE`
block). Build `06-prompt-template.py` here at the repo root, run it, iterate:

```bash
python 06-prompt-template.py
```

## Validate

When you think it's done, invoke the **validate-lab** skill. It scores your build
out of 100 against the reference, names what's missing / weaker / better, and
offers a cheat prompt if you're out of time. It pulls a pristine copy of the
reference from the companion lesson repo on the fly and cleans it up afterward —
nothing for you to install or fetch.
