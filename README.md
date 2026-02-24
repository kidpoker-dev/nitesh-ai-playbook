# Nitesh's AI Playbook

Personal repository of prompts, skills, templates, and
learnings for AI-assisted development.

---

## Structure

/prompts    — reusable instructions for Claude Code
/skills     — Claude.ai skill content (reference copies)
/templates  — CLAUDE.md starting points by project type
/learnings  — lessons from real projects

---

## How to use in any Claude Code project

Add this to your project CLAUDE.md:
```
Before starting any work, read all files in the
/docs folder of this project first.

Before running any QA, read all docs in the
/docs folder of this project first.
Then pull and apply:
github.com/[username]/nitesh-ai-playbook
/prompts/ui-qa-protocol.md

Never modify anything that appears to be an intentional
design decision without explicit confirmation from me first.
```

---

## Versioning

Every file in this repo is version controlled.
To view history of any file:
1. Open the file in GitHub
2. Click History — top right
3. Click any commit to see that version
4. Click Raw → copy → paste to roll back

Commit message convention:
- Good: "Add icon rendering rule to P1 — learned from PPT session"
- Bad:  "Update ui-qa-protocol.md"

Always write why you changed something, not just what.

---

## Files

### /prompts
- ui-qa-protocol.md — full visual and functional QA
  checklist with severity tiers P0/P1/P2/P3,
  QA loop protocol, human review flags,
  edge case checks, and final sign-off

### /skills
- product-research-framework.md — Phase 1 to 3
  framework for new app research, prototyping,
  and context doc creation before Claude Code build

### /templates
- CLAUDE_web.md — web projects
- CLAUDE_tracker.md — tracker projects
- CLAUDE_automation.md — n8n and workflow projects
- CLAUDE_analysis.md — data and dashboard projects
- CLAUDE_presentation.md — PPT and doc projects
- CLAUDE_brainstorm.md — strategy and thinking projects

### /learnings
- general/claude-code-context-management.md — always
  read /docs before QA runs, never start Claude Code
  session without full project context loaded

---

## Key Principles

1. GitHub is the master copy — Claude.ai skills are
   the deployed version. Always update GitHub first.

2. Skills live in Claude.ai — /skills folder here is
   the reference copy for version control only.

3. Templates live in GitHub — Claude Code reads them
   directly via GitHub MCP.

4. Every project gets a /docs folder — product vision,
   design decisions, intentional decisions. Claude reads
   all of it before touching any code.

5. Learnings go in immediately after every project —
   while they are fresh, not weeks later.
```

---

Commit message for this update:
```
Update README — remove test file reference, keep only real assets
