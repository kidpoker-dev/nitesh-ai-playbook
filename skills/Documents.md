---
name: pro-documents
description: Elevate all documents, reports, memos, and PDFs with clear structure, insight-driven headings, professional formatting, and strong storytelling. Auto-detects document type and adapts accordingly.
---

# Pro Documents Skill

## How This Skill Works

This skill layers ON TOP of the built-in DOCX and PDF skills. The built-in skills handle file creation (docx-js, reportlab). This skill handles **what goes into the document and how it's structured**.

When this skill conflicts with built-in defaults, **this skill wins**.

---

## Step 1: Detect Document Mode

Before writing ANY content, read the user's request and classify it:

| Mode | Trigger signals | What changes |
|------|----------------|--------------|
| **Explain/Writeup** | "document my project", "write up", "explain how I built", "case study", "blog-style", sharing with peers | Story-driven, conversational, What→Why→How→Result→Lessons flow |
| **Investor Memo** | "investor memo", "fundraise doc", "pitch document", "one-pager for VCs" | SCR arc, market data, traction, financial projections, the ask |
| **Executive Report** | "board report", "exec summary", "quarterly report", "leadership update" | Metrics-heavy, structured sections, decisions needed, risks flagged |
| **Strategy/Analysis** | "strategy doc", "analysis", "recommendation", "business case", "proposal" | Pyramid Principle, MECE, options comparison, clear recommendation |
| **How-To/Guide** | "guide", "tutorial", "how to", "documentation", "playbook", "SOP" | Step-by-step, prerequisites, examples at each step, troubleshooting |
| **Personal Notes** | "notes", "for myself", "reference doc", "cheat sheet", "summary" | Minimal formatting, dense, scannable, organized for future-you |
| **Formal Letter/Memo** | "letter", "memo", "formal communication", "notice" | Proper letterhead structure, formal tone, clear action items |

**If unsure, default to Explain/Writeup mode.**

**CRITICAL**: Do NOT inject investor/fundraise elements (TAM, competitive landscape, unit economics) unless explicitly asked. Most documents are NOT investor documents.

---

## Step 2: The Universal Rule for Documents

**Every section heading must state an insight or action, not a topic label.**

This is the document equivalent of action titles in presentations.

❌ NEVER use topic headings:
- "Background"
- "Methodology"
- "Results"
- "Discussion"
- "Architecture"

✅ ALWAYS use insight headings:
- "Freelancers lose 12% of income to payment friction — this is the problem we solved"
- "The n8n + Claude pipeline classifies 500 songs in under 3 minutes"
- "Three design decisions made the system reliable enough for daily use"
- "Switching from REST to webhooks cut processing time by 80%"
- "The main risk is Spotify API rate limits — here's how we handle them"

**The test**: Read only the section headings in sequence. They should tell the complete story. If someone reads just the table of contents and nothing else, they should understand your main argument.

**Exception**: Personal Notes and How-To/Guide modes can use shorter, more functional headings ("Prerequisites", "Step 1: Set up n8n") where clarity matters more than narrative.

---

## Step 3: Document Structure by Mode

### Explain/Writeup Mode (Default)
Use when documenting a project, sharing learnings, or writing a case study.

**Flow**: Hook → Context → What I Built → How It Works → Key Decisions → Results → Lessons

Structure:
1. **Opening paragraph** (2-3 sentences): What this is, why it matters, what the outcome was. Lead with the result, not the background.
2. **The Problem/Motivation**: What was broken, missing, or interesting. Include specific pain points with data if possible.
3. **The Approach**: High-level overview of the solution. A diagram or architecture sketch described in text.
4. **How It Works** (1-3 sections): Walk through the key components. Use subheadings for each major part.
5. **Key Decisions & Tradeoffs**: The interesting choices made and why. This is often the most valuable section.
6. **Results**: What happened. Metrics, before/after comparisons, screenshots described.
7. **What I Learned / What's Next**: Surprises, things you'd do differently, future plans.

Tone: Conversational but precise. Write like you're explaining to a smart colleague over coffee.

---

### Investor Memo Mode
Use ONLY when explicitly asked for investor-facing documents.

**Flow**: SCR Arc → Market → Solution → Traction → Team → Ask

Structure:
1. **One-line summary**: Company name + what it does + stage
2. **The Opportunity** (Situation + Complication): Market problem with data
3. **Our Solution**: What the product does and why it's different
4. **Why Now**: Market timing, regulatory shift, technology enabler
5. **Market Size**: TAM → SAM → SOM with clear assumptions
6. **Business Model**: Revenue streams, unit economics, pricing
7. **Traction**: Metrics that matter for the stage
8. **Competition**: Positioning — not a feature grid, but why you win
9. **Team**: Relevant credentials and founder-market fit
10. **The Ask**: Amount, use of funds, milestones
11. **Appendix**: Detailed financials, assumptions

Tone: Confident, data-driven, no fluff. Every sentence should either present evidence or make a claim backed by evidence.

---

### Executive Report Mode
Use for leadership updates, board reports, quarterly reviews.

Structure:
1. **Executive Summary** (first page): 5-7 sentences covering the entire document. A busy executive should be able to read ONLY this and know everything important.
2. **Key Metrics**: Table or structured list with RAG status (Red/Amber/Green)
3. **Performance**: Sections for each major area with data and trends
4. **What's Working**: Top wins with supporting evidence
5. **What's Not Working**: Issues with root cause analysis, not just symptoms
6. **Decisions Needed**: Specific decisions with options and tradeoffs
7. **Next Period Plan**: Priorities, resources, milestones
8. **Appendix**: Detailed data

Tone: Direct, factual, no spin. Flag problems early and clearly.

---

### Strategy/Analysis Mode
Use for recommendations, business cases, proposals.

**Flow**: Pyramid Principle — Answer first, then MECE supporting arguments, then evidence.

Structure:
1. **Executive Summary**: Lead with the recommendation. State what you think should happen in the first paragraph.
2. **Situation**: Current state with data
3. **Complication**: What's changed, what's broken, why action is needed now
4. **Analysis** (MECE sections): Break the problem into 3-5 non-overlapping, comprehensive areas. Each section has its own data and mini-conclusion.
5. **Options**: 2-3 strategic options compared on consistent criteria
6. **Recommendation**: Which option, why, and what it requires
7. **Implementation Plan**: Timeline, owners, milestones, dependencies
8. **Risks & Mitigations**: Two-column format — risk on left, mitigation on right
9. **Next Steps**: Immediate actions with owners and deadlines

Tone: Analytical, structured, precise. Data in every section.

---

### How-To/Guide Mode
Use for tutorials, documentation, SOPs, playbooks.

Structure:
1. **What this guide covers**: One paragraph — what you'll be able to do by the end
2. **Prerequisites**: What you need before starting (tools, access, knowledge)
3. **Steps** (numbered, sequential):
   - Each step has a clear action heading ("Step 3: Configure the n8n webhook node")
   - Each step includes what to do, why, and what success looks like
   - Include code snippets, commands, or specific values where relevant
   - Flag common mistakes or gotchas inline
4. **Verification**: How to confirm everything works
5. **Troubleshooting**: Common problems and solutions
6. **Next Steps / Related Guides**: Where to go from here

Tone: Clear, direct, imperative voice. "Click X" not "You should click X."

---

### Personal Notes Mode
Use for self-reference, knowledge capture, cheat sheets.

Structure: Whatever organization serves future-you best. Options:
- Chronological (what happened when)
- Categorical (grouped by topic)
- Decision log (what was decided and why)
- Reference card (quick-lookup format)

Tone: Shorthand is fine. Optimize for scannability. Use bold for key terms.

---

### Formal Letter/Memo Mode
Use for official communications, notices, formal requests.

Structure:
1. **Header**: Date, To, From, Subject/Re line
2. **Opening**: Purpose of the communication in one sentence
3. **Body**: Context, details, supporting information
4. **Action Items**: What you need from the recipient, with deadlines
5. **Closing**: Professional sign-off

Tone: Formal, concise, respectful. No filler.

---

## Step 4: Document Design Principles (All Modes)

### Writing Quality
- **Lead with the conclusion**: First paragraph of every section states the main point. Details follow.
- **One idea per paragraph**: If a paragraph makes two points, split it.
- **Specific over vague**: "Revenue grew 34% QoQ to ₹2.3Cr" not "Revenue grew significantly"
- **Active voice**: "The team reduced churn by 35%" not "Churn was reduced by 35%"
- **Cut ruthlessly**: If a sentence doesn't add information, delete it.

### Formatting
- **Heading hierarchy matters**: H1 for major sections, H2 for subsections, H3 sparingly. Never skip levels.
- **Short paragraphs**: Max 4-5 sentences. Dense paragraphs are hard to scan.
- **Strategic use of bold**: Bold key findings, metrics, and action items. Don't bold everything.
- **Tables for comparisons**: Any time you're comparing 2+ things on 3+ criteria, use a table.
- **Bullet points sparingly**: Use for lists of 3-7 items. For fewer, use inline prose. For more, use a table.
- **Pull quotes / callout boxes**: Use for the single most important insight in each section.

### Visual Hierarchy in Documents
- **Title**: Large, bold, clear
- **Section headings**: Bold, slightly larger than body, with spacing above
- **Body text**: Consistent font, comfortable reading size (11-12pt)
- **Captions and footnotes**: Smaller, lighter color
- **Page numbers**: Bottom of every page

### Data Presentation
- **Tables**: For exact values and comparisons
- **Inline metrics**: Bold the number — "The system processed **847 songs** in **2 minutes 43 seconds**"
- **Before/after framing**: Always show the contrast when presenting improvements
- **Source everything**: Add source notes for any external data point

---

## Step 5: Anti-Patterns (Things to NEVER Do)

### Structural
- ❌ Topic headings ("Background", "Methodology") instead of insight headings
- ❌ Burying the conclusion at the end — always lead with it
- ❌ Wall of text with no subheadings (max 3 paragraphs before a subheading)
- ❌ Starting with "In today's rapidly evolving landscape..." or any throat-clearing opener
- ❌ Using TAM/business model/financials when not asked for an investor document
- ❌ Ending with "In conclusion, ..." — the document structure should make the conclusion obvious

### Content
- ❌ Buzzword soup ("leveraging synergies", "paradigm shift", "holistic approach")
- ❌ Passive voice throughout ("it was determined that..." → "we determined...")
- ❌ Vague claims without evidence ("significant improvement" → "34% improvement")
- ❌ Repeating the same point in different sections with different words
- ❌ Long introductions before getting to the point

### Formatting
- ❌ Inconsistent heading styles across sections
- ❌ Walls of bullets (more than 7 bullets in a row)
- ❌ Bold AND italic AND underline on the same text
- ❌ Multiple fonts in the same document
- ❌ No page numbers on multi-page documents

---

## Step 6: The Heading Test (Before Writing)

Before writing any content, draft just the headings in sequence. Read them:

1. Do they tell a coherent story?
2. Would someone reading ONLY the headings understand the main message?
3. Does each heading state a specific insight (not a topic label)?
4. Is there a clear beginning (context), middle (substance), and end (so-what)?

If any answer is no, fix the headings before writing content.

---

## Reference: Quick Decision Guide

User says... → Use this mode:
- "document my project" / "write up what I built" → **Explain/Writeup**
- "investor memo" / "pitch document" → **Investor Memo**
- "quarterly report" / "board report" → **Executive Report**
- "analyze whether we should..." / "recommendation on..." → **Strategy/Analysis**
- "create a guide for..." / "write documentation for..." → **How-To/Guide**
- "notes for myself" / "cheat sheet" → **Personal Notes**
- "write a formal letter to..." / "draft a memo" → **Formal Letter/Memo**
- "create a document" (no other context) → **Ask the user** what it's for, then route
