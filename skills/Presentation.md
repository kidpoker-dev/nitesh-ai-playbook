---
name: pro-presentations
description: Elevate all presentations with action titles, clear storytelling, smart layouts, and professional structure. Auto-detects presentation type and adapts accordingly.
---

# Pro Presentations Skill - V2
This is the updated version of this skill.

## How This Skill Works

This skill layers ON TOP of the built-in PPTX skill. The built-in skill handles file creation (PptxGenJS, shapes, charts). This skill handles **what goes on the slides and how it's structured**.

When this skill conflicts with built-in PPTX defaults, **this skill wins**.

---

## Step 1: Detect Presentation Mode

Before creating ANY slide, read the user's request and classify it:

| Mode | Trigger signals | What changes |
|------|----------------|--------------|
| **Explain** | "explain to", "show my friend", "walk through", "how I built", "document my project", personal notes, learning summary | Story-driven, casual tone, What→Why→How→Result flow, visuals over data |
| **Pitch/Fundraise** | "pitch deck", "investor", "fundraise", "VC", "seed round", "series A" | Full SCR arc, TAM/SAM/SOM, traction, financial projections, the ask |
| **Board/Executive** | "board update", "leadership review", "exec summary", "quarterly review" | Metrics-heavy, status updates, risks, decisions needed, conservative design |
| **Strategy/Analysis** | "strategy", "analysis", "recommendation", "proposal", "business case" | Frameworks, MECE structure, data-driven, clear recommendations |
| **Teach/Workshop** | "training", "workshop", "tutorial", "teach", "onboarding" | Progressive complexity, examples on every slide, exercises, recap slides |
| **Personal Notes** | "notes", "for myself", "document", "keep track", "reference" | Minimal design, content-dense, organized for future reference |

**If unsure, default to Explain mode** — it produces the most universally useful output.

**CRITICAL**: Do NOT use Pitch/Fundraise elements (TAM, business model, competitive landscape, financial projections) unless the user explicitly asks for a pitch deck or investor presentation. Most presentations are NOT pitch decks.

---

## Step 2: Apply the One Universal Rule

**Every slide title must be a complete sentence that states the insight or takeaway.**

This applies to ALL modes, every single time. No exceptions.

❌ NEVER use topic titles:
- "Market Overview"
- "Project Architecture"  
- "Key Findings"
- "Next Steps"
- "About Me"

✅ ALWAYS use action titles:
- "India's freelancer payment market reaches $12B with 70% unserved by digital rails"
- "The n8n workflow processes 500 songs in 3 minutes using mood-based classification"
- "Three architectural choices made this system 10x faster than the initial approach"
- "We need to decide on pricing model before the March launch"
- "I automated my entire Spotify library in one weekend using Claude + n8n"

**The test**: Read only the titles of all slides in sequence. They should tell a complete, coherent story on their own. If someone reads just the titles and skips everything else, they should understand your main message.

---

## Step 3: Structure by Mode

### Explain Mode (Default)
Use when sharing a project, idea, or experience with peers, friends, or general audiences.

**Flow**: Context → What I Did → How It Works → Key Decisions → Results → What I Learned

Typical 6-10 slides:
1. **Hook**: One-sentence summary of what this is and why it matters (action title IS the hook)
2. **The Problem/Motivation**: Why you did this — what was broken, missing, or interesting
3. **The Approach**: High-level overview of your solution (diagram or 3-step flow)
4. **How It Works (1-3 slides)**: Walk through the key components, show architecture/workflow
5. **Key Decision**: One interesting tradeoff or choice you made and why
6. **Results/Demo**: What happened — metrics, screenshots, before/after
7. **Lessons Learned**: What surprised you, what you'd do differently
8. **What's Next** (optional): Future plans or open questions

Design: Casual, visual, use screenshots and diagrams. Lighter color palette. Conversational tone.

---

### Pitch/Fundraise Mode
Use ONLY when explicitly asked for investor/VC presentations.

**Flow**: SCR Arc (Situation → Complication → Resolution) + Evidence + Ask

The Sequoia/YC hybrid structure (10-12 slides):
1. **Cover**: Company name + one-line description
2. **Problem**: Pain point with data showing magnitude
3. **Solution**: Your product — what it does, not how
4. **Why Now**: Market timing, regulatory shift, technology enabler
5. **Market Size**: TAM → SAM → SOM with clear assumptions
6. **Product**: Screenshots, demo, how it works
7. **Business Model**: Revenue streams, unit economics, pricing
8. **Traction**: Metrics that matter for your stage
9. **Competition**: 2x2 positioning matrix (NOT a feature checklist)
10. **Team**: Photos + relevant credentials + why THIS team
11. **The Ask**: Amount + use of funds + milestones it unlocks
12. **Appendix**: Detailed financials, assumptions, backup slides

Design: Professional, authoritative. Dark title slides, light content slides. Minimal decoration.

---

### Board/Executive Mode
Use for leadership updates, quarterly reviews, performance reporting.

**Flow**: Headlines → Performance → Issues → Decisions Needed

Typical 8-15 slides:
1. **Executive Summary**: 3-5 bullet synthesis of everything (this is the ONE slide they'll read)
2. **Key Metrics Dashboard**: Traffic-light status (green/yellow/red) on 5-8 KPIs
3. **Performance Deep-Dive (2-4 slides)**: Charts with trend data, YoY/QoQ comparisons
4. **What's Working**: Top 2-3 wins with supporting data
5. **What's Not Working**: Top 2-3 risks/issues with root cause
6. **Decisions Needed**: Specific decisions with options and trade-offs
7. **Next Quarter Plan**: Priorities, resource allocation, key milestones
8. **Appendix**: Detailed data tables for reference

Design: Conservative, data-dense. Tables and charts dominate. Minimal visual flair.

---

### Strategy/Analysis Mode
Use for recommendations, business cases, consulting-style deliverables.

**Flow**: Pyramid Principle — Answer first, then MECE supporting arguments, then evidence

Typical 10-20 slides:
1. **Cover**: Title + date + author
2. **Executive Summary**: Recommendation upfront with 3-5 supporting points
3. **Situation**: Current state with data
4. **Complication**: What's changed or what's broken
5. **Analysis (3-6 slides)**: MECE breakdown of the problem, each with data
6. **Options**: 2-3 strategic options compared on key criteria
7. **Recommendation**: Clear choice with rationale
8. **Implementation Plan**: Timeline, owners, milestones
9. **Risks & Mitigations**: 2-column format
10. **Next Steps**: Immediate actions with deadlines

Design: Clean, structured. Frameworks and matrices. Consistent formatting throughout.

---

### Teach/Workshop Mode
Use for training, tutorials, onboarding, educational content.

**Flow**: Why This Matters → Concept → Example → Practice → Recap

Typical structure (scales to content):
1. **Hook**: Why should the audience care about this topic
2. **Learning Objectives**: 3-4 things they'll know by the end
3. **Concept Slides**: One concept per slide, built progressively
4. **Example Slides**: Real examples for each concept
5. **Practice/Exercise** (if applicable): Hands-on activity
6. **Common Mistakes**: What to watch out for
7. **Recap**: Reinforce the 3-4 key takeaways
8. **Resources**: Where to learn more

Design: Engaging, visual. Progressive disclosure. Icons and diagrams over text. More white space.

---

### Personal Notes Mode
Use for self-reference, documentation, knowledge capture.

**Flow**: Whatever organization serves future-you best

Design: Minimal, content-dense. Function over form. Clear headings, scannable structure.

---

## Step 4: Slide Design Principles (All Modes)

### Layout Variety (Critical)
**NEVER use the same layout on consecutive slides.** Alternate between:
- Two-column (text + visual)
- Full-width chart/diagram
- Big number callout (metric + context)
- Icon grid (3-4 items with icons)
- Screenshot with annotation callouts
- Comparison columns (before/after, option A/B)
- Process flow (horizontal steps)
- Quote or testimonial highlight

### Content Density
- **Max 5 bullet points per slide** (prefer 3)
- Each bullet is **1-2 sentences**, not a paragraph
- If a slide has >40 words of body text, split it into two slides
- **One idea per slide** — if you need "and" in the title, it's probably two slides

### Visual Hierarchy
- Action title: 18-20pt bold, prominent color
- Body text: 12-14pt, dark gray (not black)
- Source/footnote: 8-9pt, light gray, bottom of slide
- Slide number: bottom-right, subtle
- **Size contrast matters**: Title must be visually dominant

### Data Visualization
- Bar/column chart: Comparing quantities across categories
- Line chart: Showing trends over time
- Pie/donut: Parts of a whole (max 5 segments)
- Big number callout: When one stat tells the story
- Table: When exact values matter more than patterns
- **ALWAYS annotate charts** — add a callout or highlight pointing to the insight
- **NEVER show a chart without explaining what to see in it**

---

## Step 5: Anti-Patterns (Things to NEVER Do)

### Structural
- ❌ Topic titles ("Market Overview") instead of action titles
- ❌ Same layout repeated on 3+ consecutive slides
- ❌ Wall of text (>6 bullets or >50 words body text)
- ❌ Slides that could be reordered without losing narrative flow
- ❌ Ending with "Thank You" or "Questions?" — end with a takeaway or call-to-action
- ❌ Using TAM/SAM/SOM, business models, or financials when not asked for a pitch deck
- ❌ Generic agenda slides that add no insight

### Design
- ❌ Accent underlines below titles (hallmark of AI-generated slides)
- ❌ Purple/blue gradient backgrounds
- ❌ Center-aligned body text (left-align always, center only titles)
- ❌ Charts without annotations or callouts
- ❌ Inconsistent margins across slides
- ❌ More than 3-4 colors total
- ❌ Drop shadows on everything
- ❌ Decorative elements that don't serve the content

### Content
- ❌ Buzzword soup ("leveraging synergies to drive paradigm shifts")
- ❌ Vague claims without data ("significant growth")
- ❌ Repeating the same point across multiple slides with different words

---

## Step 6: The Ghost Deck Check (Before Designing)

Before creating any visual slides, mentally draft a "ghost deck" — just the titles in sequence. Read them aloud:

1. Do they tell a coherent story?
2. Would someone reading ONLY the titles understand the main message?
3. Does each title state a specific insight (not a topic label)?
4. Is there a clear beginning, middle, and end?

If any answer is no, fix the titles before proceeding to design.

---

## Reference: Quick Decision Guide

User says... → Use this mode:
- "make a presentation about my project" → **Explain**
- "pitch deck for investors" → **Pitch/Fundraise**
- "quarterly board update" → **Board/Executive**  
- "analyze whether we should enter market X" → **Strategy/Analysis**
- "create training slides on topic X" → **Teach/Workshop**
- "document my workflow for reference" → **Personal Notes**
- "make me a presentation" (no other context) → **Ask the user** what it's for, then route
