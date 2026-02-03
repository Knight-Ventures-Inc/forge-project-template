# Inbox — Frame Phase Workflow

This directory supports the inbox-driven Frame (F) phase workflow.

---

## How It Works

### 1. Drop Discovery Materials

Create a folder in `00_drop/` with your feature slug:

```
inbox/00_drop/my-feature/
├── README.md          ← Required: describe what you want
├── threads/           ← Transcripts, notes, brain dumps
├── assets/            ← Sketches, screenshots, photos
└── links.md           ← External references (optional)
```

### 2. Product Strategist Processes

The Product Strategist agent:
1. Reads your discovery materials
2. Asks clarifying questions (up to 3 rounds)
3. Synthesizes into coherent product intent
4. Produces Product Intent Packet

### 3. Output Delivered

Product Intent Packet appears in `10_product-intent/`:

```
inbox/10_product-intent/my-feature/
├── README.md
├── intent.md
├── actors.md
├── use-cases.md
├── non-goals.md
├── assumptions.md
├── open-questions.md
└── source-index.md
```

### 4. Human Routes

Human Lead reviews packet and routes to next phase (Project Architect).

---

## Directory Structure

```
inbox/
├── README.md              ← You are here
├── 00_drop/               ← Discovery input (you write here)
│   └── .template/         ← Example structure
└── 10_product-intent/     ← Product Intent Packets (agent writes here)
    └── .template/         ← Example packet
```

---

## When to Use This

- **New feature:** Drop discovery for any new capability
- **Bug/refactor:** When clarification needed before fixing
- **Pivot:** When direction is changing significantly
- **Enhancement:** When scope needs definition

---

## Quality Expectations

Product Intent Packets are professional PM-level artifacts:
- Usable by external development teams
- Clear enough for stakeholder review
- Complete enough for technical planning

---

## Relationship to Other Artifacts

| Artifact | Purpose | Location |
|----------|---------|----------|
| Product Intent Packet | Frame-phase discovery output | `inbox/10_product-intent/` |
| PRODUCT.md | Refined constitutional doc | `docs/constitution/` |
| Task briefs | Execute-phase work packets | `ai_prompts/active/` |

Product Intent Packets **precede and inform** PRODUCT.md.
They are preserved as historical discovery record.
