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

Figma lets you iterate on pixels—layout, color, spacing. DNA lets you iterate on the decisions that actually matter—what problem you're solving, what tradeoffs you're making, what principles govern when rules conflict.

DNA makes the invisible visible. And visible means iterable.

---

## Install

**One-line install (recommended):**

```bash
npx skills add tylercecchi/product-design-skills --skill design-dna
```

**Or manual:**

```bash
mkdir -p .claude/skills/design-dna && curl -sS https://raw.githubusercontent.com/tylercecchi/product-design-skills/main/SKILL.md -o .claude/skills/design-dna/SKILL.md
```

---

## Usage

Open Claude Code and say:

```
start new dna
```

That's it. Claude will guide you through building your DNA.

### Commands

**Building**
- `start new dna` — Begin with Foundations
- `work on [layer]` — Build or edit any layer

**Viewing**
- `show [layer]` — Display current content
- `show all` — Overview of all layers

**Reviewing**
- `review` — Check completeness
- `review problem space` — Review Part 1
- `review product definition` — Review Part 2
- `review design system` — Review Part 3

**Visualizing**
- `visualize [layer]` — Interactive graph with clickable previews
- `visualize all` — Full DNA map
- `generate reference app` — Living style guide

**Experimenting**
- `try [change]` — Preview in code
- `keep it` — Sync to DNA
- `revert` — Restore from DNA

---

## What DNA Does

DNA encodes the logic of a product's design in three parts:

### Part 1: Problem Space
*The real design work. Where your judgment matters most.*

- **Foundations** — What is this? What's its posture?
- **Problem Statement** — What's broken? For whom?
- **Friction Map** — Where does pain concentrate?
- **User Forces** — What pushes change? What pulls back?
- **Success Criteria** — What does "solved" look like?
- **Anti-goals** — What are you *not* solving?

### Part 2: Product Definition
*What you're building.*

- **Schema** — What entities exist? (the nouns)
- **Genome** — What can users do? (the verbs)
- **Principles** — What values guide tradeoffs?

### Part 3: Design System
*How it looks and behaves.*

- **Tokens** — Raw values (timing, spacing, color)
- **Appearances** — How entities look
- **Conditions** — How context changes behavior
- **Modules** — Interaction patterns
- **Examples** — Worked demonstrations

Everything is connected. Change a principle, the whole product shifts. Add a friction point, gaps surface automatically.

---

## Why DNA Matters

Design tools show you pixels. DNA shows you the system.

In Figma, you're arranging rectangles. You don't see what entity a card represents, what states it has, what principles govern it.

In DNA, you design the logic. The UI is a consequence.

**The designer's role elevates.** Less pixel-pushing. More systems thinking. You're not designing screens—you're designing the machine that generates screens.

Claude handles fabrication. You handle judgment.

---

## Files

When you build a DNA, this structure is created:

```
dna/
└── [product-name]/
    ├── foundations.md
    ├── problem.md
    ├── success.md
    ├── anti-goals.md
    ├── schema.md
    ├── genome.md
    ├── principles.md
    ├── tokens.yaml
    ├── appearances.md
    ├── conditions.md
    ├── modules.md
    ├── examples.md
    ├── references/
    └── visualizations/
```

---

## License

MIT

---

**Design the logic. The pixels follow.**
