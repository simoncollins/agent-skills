---
name: article-drafting
description: Draft articles collaboratively using markdown files for iterative annotation. Supports writing opinion pieces and how-to articles with type-specific templates and a structured discovery-to-draft workflow.
---

# Skill: Article Drafting

A collaborative process for developing articles using markdown files for iterative annotation. Supports multiple article types with type-specific templates.

## Supported Article Types

### Opinion Pieces
- Arguments, predictions, prescriptions
- Thought leadership content
- Essays with a clear thesis
- **Templates:** `templates/opinion/`

### How-To Articles
- Tutorials and guides
- Process explanations
- Step-by-step instructions
- **Templates:** `templates/howto/`

## Article Type Detection

Detect article type from the user's prompt:

- **Opinion piece** if prompt mentions: opinion, argument, thesis, thought leadership, prediction, essay, position, perspective
- **How-to** if prompt mentions: how-to, how to, guide, tutorial, process, steps, instructions, walkthrough

If unclear, ask: "Is this an opinion piece (arguing a position) or a how-to (teaching a process)?"

## Workflow

### Phase 1: Discovery
Create questionnaire from the appropriate template. Author annotates with `>` responses.

- Opinion: `templates/opinion/questionnaire-template.md`
- How-to: `templates/howto/questionnaire-template.md`

**Output:** `[topic]-questionnaire-01.md`

### Phase 2: Critique
Stress-test using the appropriate template. Author responds to challenges.

- Opinion: `templates/opinion/critique-template.md` (focus: is argument sound?)
- How-to: `templates/howto/critique-template.md` (focus: can readers follow?)

**Output:** `[topic]-critique.md`

### Phase 3: Understanding
Summarise thesis/approach as understood. Get author confirmation before proceeding.

**Output:** `[topic]-understanding.md`

### Phase 4: Structure
Propose 2-3 narrative options from the appropriate template. Author chooses.

- Opinion: `templates/opinion/structure-options.md`
- How-to: `templates/howto/structure-options.md`

**Output:** `[topic]-structure-options.md`

### Phase 5: Outline
Section-by-section plan with word counts and key points.

**Output:** `[topic]-detailed-outline.md`

### Phase 6: Draft
Write article following `writing-principles.md`.

**Output:** `[topic]-draft-v1.md`

### Phase 7: Assets
Create supporting materials:

**Both types:**
- Teaser/TLDR (150-300 words for social)
- Visual interest (pull quotes, diagram ideas)

**Opinion pieces:**
- Follow-up article ideas

**How-to articles:**
- Parking lot (running ideas captured throughout session)

**Outputs:** `[topic]-teaser.md`, `[topic]-visual-interest.md`, `[topic]-followup-articles.md` or `[topic]-parking-lot.md`

## Folder Organization

Create a dedicated folder for each article draft:

```
drafts/
  [topic]/
    [topic]-questionnaire-01.md
    [topic]-critique.md
    [topic]-understanding.md
    ...
```

This keeps all working files for an article together and makes it easy to manage multiple drafts in progress.

## Key Principles

1. **Use files, not chat** - Create markdown files for annotation rather than conversational Q&A
2. **Critique before writing** - Stress-test arguments/approaches early
3. **Confirm understanding** - Write back what you understood before drafting
4. **Offer structure choices** - Present narrative options with trade-offs
5. **Concrete examples matter** - Push for specific illustrations in discovery

## Invocation

Begin with:

> "I'll help you develop this into a polished article. We'll work collaboratively using markdown files you can annotate."

Then:
1. Detect or ask about article type
2. Create the Phase 1 questionnaire file using the appropriate template

