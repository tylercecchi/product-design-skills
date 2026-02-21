```
╔═══════════════════════════════════════════════════════════════╗
║                                                               ║
║     ██████╗ ███╗   ██╗ █████╗                                 ║
║     ██╔══██╗████╗  ██║██╔══██╗                                ║
║     ██║  ██║██╔██╗ ██║███████║                                ║
║     ██║  ██║██║╚██╗██║██╔══██║                                ║
║     ██████╔╝██║ ╚████║██║  ██║                                ║
║     ╚═════╝ ╚═╝  ╚═══╝╚═╝  ╚═╝                                ║
║                                                               ║
║     Product Design DNA                                        ║
║     Designed by Tyler Cecchi                                  ║
║                                                               ║
║     Design the logic. The pixels follow.                      ║
║                                                               ║
╚═══════════════════════════════════════════════════════════════╝
```

# Product Design DNA

**DNA is a canvas for iterating on design concepts and logic, the same way Figma lets you iterate on pixels.**

---

## How It Works

1. **Scaffold** — Create a DNA with all files ready to fill
2. **Add to DNA** — Describe friction, entities, appearances, etc.
3. **Fabricate** — Code is generated from your DNA
4. **Iterate** — Change DNA, code updates to match

DNA drives code. Not the other way around.

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│   DNA Files                        Code                 │
│                                                         │
│   ┌──────────────┐                                      │
│   │ friction.md  │───┐                                  │
│   └──────────────┘   │                                  │
│   ┌──────────────┐   │         ┌──────────────────┐     │
│   │ schema.md    │───┼────────▶│ Components.tsx   │     │
│   └──────────────┘   │         └──────────────────┘     │
│   ┌──────────────┐   │         ┌──────────────────┐     │
│   │ appearances  │───┼────────▶│ Styles           │     │
│   └──────────────┘   │         └──────────────────┘     │
│   ┌──────────────┐   │         ┌──────────────────┐     │
│   │ modules.md   │───┼────────▶│ Interactions     │     │
│   └──────────────┘   │         └──────────────────┘     │
│   ┌──────────────┐   │                                  │
│   │ tokens.yaml  │───┘                                  │
│   └──────────────┘                                      │
│                                                         │
│   Change DNA ──────────────────▶ Code refabricates      │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## Install

**One-line install (recommended):**

```bash
npx skills add tylercecchi/product-design-skills --skill design-dna
```

**Or manual:**

```bash
mkdir -p .claude/skills/design-dna && curl -sS https://raw.githubusercontent.com/tylercecchi/product-design-skills/skills/design-dna/SKILL.md -o .claude/skills/design-dna/SKILL.md
```

---

## Quick Start

```
> start new dna

What are you designing?

> a task manager for freelancers

Got it. Quick setup:

Name: Freelance Tasks
Platform: (web / mobile / desktop / cross-platform)?

> web

Component library: (shadcn / Radix / Material / none)?

> shadcn

Posture—how should it feel? (calm / fast / playful / professional)?

> fast and minimal

CREATING DNA:
✓ foundations.md (populated)
✓ friction.md (ready to capture)
✓ success.md (ready to capture)
✓ mental-models.md (ready to capture)
✓ constraints.md (ready to capture)
✓ schema.md (ready to capture)
✓ appearances.md (ready to capture)
✓ ... all files scaffolded

✓ dna-map.html (visualization)

Open dna-map.html to see your DNA structure.

Ready to build. What's the first thing a user should see?

> a list of their projects

CREATING DNA:
- schema.md: Project entity (title, status, updated_at)
- appearances.md: ProjectList, ProjectCard
- tokens.yaml: Using shadcn defaults

FABRICATING:
- ProjectList.tsx
- ProjectCard.tsx

Here's a starting point. What feels wrong?
```

---

## The DNA Files

When you create a DNA, all files are scaffolded so you can see what's available to define:

### Problem Space (what you're solving)

| File | What it captures | How it drives fabrication |
|------|------------------|---------------------------|
| `friction.md` | Pain points, struggles | Prioritizes what to build, validates changes |
| `success.md` | What "solved" looks like | Validates that design achieves goals |
| `mental-models.md` | How users think | Shapes metaphors, interactions |
| `constraints.md` | Limitations (technical, user) | Defines boundaries, conditions |
| `user-forces.md` | What pushes/pulls users | Guides onboarding, reduces resistance |
| `anti-goals.md` | What's out of scope | Blocks scope creep |

### Product Definition (what you're building)

| File | What it captures | How it drives fabrication |
|------|------------------|---------------------------|
| `schema.md` | Entities (the nouns) | Creates data structures, components |
| `genome.md` | Actions (the verbs) | Creates interactions, flows |
| `principles.md` | Tradeoff priorities | Resolves design conflicts |

### Design System (how it looks and behaves)

| File | What it captures | How it drives fabrication |
|------|------------------|---------------------------|
| `tokens.yaml` | Colors, spacing, timing | Generates CSS variables, theme |
| `appearances.md` | How entities look | Generates component styles |
| `conditions.md` | Context-based changes | Generates responsive/state logic |
| `modules.md` | Interaction patterns | Generates animations, behaviors |

---

## How Layers Connect

DNA layers aren't isolated—they constrain and inform each other.

```
PROBLEM SPACE (why)
├── Friction ──────────┐
├── Success Criteria   │
├── Mental Models      ├──▶ Validates every decision
├── Constraints        │
└── Principles ────────┘
         │
         ▼
PRODUCT DEFINITION (what)
├── Schema (entities) ─────┬──▶ What exists
└── Genome (actions) ──────┘    What users can do
         │
         ▼
DESIGN SYSTEM (how)
├── Tokens (values) ───────┐
├── Appearances (visuals) ─┼──▶ How it looks and behaves
├── Modules (behaviors) ───┘
└── Conditions (context)
         │
         ▼
      CODE
```

### Example: "Add quick task creation"

```
> I need users to add tasks without leaving the current view

CHECKING PROBLEM SPACE:
✓ Friction: "Too many clicks to add tasks" — this addresses it
✓ Success: "Add task in <3 seconds" — this helps
✓ Mental Models: Users expect inline creation (like iOS Reminders)
✓ Principles: #1 "Speed over ceremony" — supports inline

CHECKING PRODUCT DEFINITION:
✓ Schema: Task entity exists
⚠️ Genome: "Create Task" currently requires modal

CHECKING DESIGN SYSTEM:
⚠️ Appearances: No inline input defined
✓ Modules: "expand-in-place" exists, could use it
✓ Tokens: timing.expand = 150ms

UPDATING DNA:
- genome.md: "Create Task" → adding inline trigger
- appearances.md: Adding QuickAddInput
- modules.md: Applying expand-in-place

FABRICATING:
- QuickAddInput.tsx (new)
- TaskList.tsx (updated)

✓ Done
```

Every layer contributed:
- **Friction** validated the need
- **Mental Models** shaped the pattern (inline like iOS)
- **Principles** resolved the choice (speed > ceremony)
- **Genome** defined what happens
- **Modules** defined how it animates

### Conflicts Surface Automatically

```
> add a confirmation dialog before deleting

CHECKING DNA:
- Genome: Delete is "reversible" (undo available)
- Principles: #2 "Forgiveness over prevention"

⚠️ CONFLICT:
Confirmation is prevention. But Delete is reversible, 
and your principles favor forgiveness.

Options:
1. Skip confirmation, show undo toast (honor principles)
2. Add confirmation anyway (override for this case)
3. Make Delete "destructive" (permanent, needs confirmation)

> option 1

✓ No changes needed. Delete already shows undo toast.
```

The layers check each other. Conflicts surface before code is written.

---

## Adding to DNA

You can add to DNA files directly, or just describe what you want:

### Direct editing
```markdown
<!-- In friction.md -->

## Major Friction

- **Status visibility**: Users can't quickly see project status
  - Impact: Wastes time, causes anxiety
  - Must address: Yes
```

### Through conversation
```
> users can't quickly see project status, it's causing anxiety

Adding to DNA:
- friction.md: "Status visibility" (major)

This affects ProjectCard. Status should be prominent.

UPDATING:
- appearances.md: ProjectCard → status prominence increased

REFABRICATING:
- ProjectCard.tsx

Done.
```

Either way, DNA updates → code refabricates.

---

## The Visualization

When DNA is created, `dna-map.html` is generated. Open it to see:

- Every layer and what's in it
- Connections between layers (friction → schema → appearances)
- Click any node to preview it
- Updates live as DNA changes

Keep it open alongside your work. It's your map of the system.

---

## Iteration Loop

The core loop is:

```
1. See something wrong
          ↓
2. Describe the change (or edit DNA directly)
          ↓
3. DNA updates
          ↓
4. Code refabricates
          ↓
5. See the result
          ↓
   (repeat)
```

**Examples:**

```
> the cards feel too cramped

What specifically feels cramped?
- Too much content?
- Not enough spacing?
- Both?

> not enough spacing

UPDATING DNA:
- tokens.yaml: spacing.card increased
- appearances.md: ProjectCard padding → scale[4]

REFABRICATING:
- ProjectCard.tsx
- TaskCard.tsx (uses same token)

✓ 2 components updated
```

```
> add a way to archive projects

Adding to DNA:
- genome.md: "Archive Project" action
- schema.md: Project → adding "archived" state
- appearances.md: ProjectCard → archived variant

FABRICATING:
- ArchiveButton.tsx
- ProjectCard archived state

Done. Where should the archive button appear?
```

```
> actually, archiving is out of scope for v1

Adding to DNA:
- anti-goals.md: "Archiving projects"

REMOVING:
- genome.md: Archive Project action
- schema.md: archived state
- Related components

Done. Archiving blocked for v1.
```

---

## Commands

| Command | What it does |
|---------|--------------|
| `start new dna` | Scaffold DNA, create visualization, start building |
| `visualize map` | Interactive dependency graph (system view) |
| `visualize dna` | Scrollable documentation (reference view) |
| `undo` | Revert last DNA change, refabricate |
| `check for updates` | Update the skill, migrate DNA if needed |

Most interaction is natural language. Just describe what you want:

```
> add a swipe gesture to dismiss cards

Checking DNA...

SCHEMA: ✓ Card entity exists
MODULES: ⚠️ No swipe module defined
GENOME: ? What does swiping do?

> dismiss the card

UPDATING DNA:
- modules.md: Adding swipe-dismiss
- genome.md: Adding "Dismiss Card" action
- appearances.md: Card → swipe affordance

FABRICATING:
- Card.tsx updated

✓ Done
```

Claude figures out which layers are involved, checks for conflicts, asks clarifying questions, then updates DNA and fabricates.

---

## Why DNA

In Figma, you iterate on pixels. In DNA, you iterate on decisions.

- **Friction Map** isn't documentation—it drives what gets built
- **Principles** aren't a manifesto—they resolve conflicts automatically
- **Schema** isn't a data model—it generates components
- **Appearances** aren't mockups—they fabricate code

Change the DNA, the product changes. The system stays coherent because everything flows from the same source of truth.

**Design the logic. The pixels follow.**

---

## License

MIT
