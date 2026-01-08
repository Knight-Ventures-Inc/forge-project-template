# FORGE-SD Project Template

**A FORGE-governed software development project.**

---

## FORGE Canon Reference

This project operates under **The FORGE Method(TM)**.

**Canonical Authority:**
- FORGE Core: [FORGE-Method/core/forge-core.md](https://github.com/Knight-Ventures-Inc/FORGE-Method)
- Operations: [FORGE-Method/core/forge-operations.md](https://github.com/Knight-Ventures-Inc/FORGE-Method)
- SD Profile: [FORGE-Method/profiles/forge-sd-profile.md](https://github.com/Knight-Ventures-Inc/FORGE-Method)

> **Rule:** This repo does not redefine FORGE. It *consumes* FORGE by reference.
> If methodology questions arise, consult the canon.

---

## Project Identity

### What This Is
[CUSTOMIZE: 2-3 sentences describing the project's purpose]

### What This Is NOT
- [CUSTOMIZE: Explicit non-goal 1]
- [CUSTOMIZE: Explicit non-goal 2]
- [CUSTOMIZE: Explicit non-goal 3]

### Who This Is For
- **Primary users:** [CUSTOMIZE: Who uses this directly]
- **Stakeholders:** [CUSTOMIZE: Who cares about outcomes]

---

## Constitution Check (CC: Read This First)

**Before any work, check constitutional status:**

```
docs/constitution/
├── PRODUCT.md        # Product intent (North Star)
├── TECH.md           # Technical architecture
└── GOVERNANCE.md     # Security, permissions, policies
```

### If Constitution Is Empty or Missing

**STOP.** Do not scaffold. Do not implement.

Request from Human Lead:
1. Product brief / North Star document
2. Technical decisions / architecture constraints
3. Governance rules (auth, RLS, security requirements)

The constitution must exist before Execute phase begins.

### If Constitution Exists

Proceed with scaffolding and execution per the constitution.

---

## Agent Lanes

| Role | Agent | Authority | Boundary |
|------|-------|-----------|----------|
| **Human Lead** | [CUSTOMIZE] | Final decisions, greenlight, merge | Reviews, approves, resolves |
| **Strategist** | Jordan (ChatGPT) | Business strategy, feature framing | Does NOT implement |
| **Spec Author** | CP (Claude Project) | Constitutional docs, specs | Does NOT create PRs |
| **Quality Gate** | CC (Claude Code) | Verification, PRs, build-plan | Does NOT make arch decisions |
| **Implementation** | Cursor | Code per task briefs | Does NOT create PRs |

### Lane Rules

- **Strategist and Spec Author** communicate bidirectionally (through Human Lead)
- **Specs flow one-way** to Quality Gate (no modifications)
- **Quality Gate and Implementation** cycle tightly
- **Implementation Engine never communicates** with Strategist or Spec Author

---

## Current State

### Phase
[CUSTOMIZE: Frame | Orchestrate | Refine | Govern | Execute]

### If In Execute
- **Current PR:** [PR-XX or "None"]
- **Build Plan:** `docs/build-plan.md`
- **Active Brief:** `ai_prompts/active/`
- **Ops State:** `docs/ops/state.md`

---

## Commands

### Verification Sequence (Sacred Four)
```bash
pnpm typecheck && pnpm lint && pnpm test:run && pnpm build
```
**All four must pass before any PR. No exceptions.**

### Development
```bash
pnpm dev          # Start development server
pnpm build        # Production build
```

### Database (if using Supabase)
```bash
pnpm db:generate  # Generate migrations
pnpm db:migrate   # Apply migrations
```

---

## Non-Negotiables

1. **Constitution before Execute** — No constitutional docs = no scaffolding
2. **Verification runs before every PR** — Sacred Four, all must pass
3. **Constitutional docs are read-only** — Suggest changes, don't modify
4. **5-line rule** — < 5 lines: CC fixes; >= 5 lines: back to Cursor
5. **File-based handoffs** — Everything through `ai_prompts/`
6. **Archive before starting** — Each PR archives the previous brief

---

## Getting Oriented (CC Session Start)

```
1. Read this file (you're doing it)
2. Check docs/constitution/ — if empty, STOP and request inputs
3. Check docs/build-plan.md for current PR
4. Run: git log --oneline -5
5. Check ai_prompts/active/ for current brief
6. Ready to proceed (~90 seconds)
```

---

## Key Locations

| What | Where |
|------|-------|
| Constitution | `docs/constitution/` |
| Build Plan | `docs/build-plan.md` |
| Ops State | `docs/ops/state.md` |
| Current Brief | `ai_prompts/active/` |
| Completed Briefs | `ai_prompts/completed/` |
| Templates | `ai_prompts/templates/` |
| ADRs | `docs/adr/` |

---

## Technical Stack

| Layer | Technology |
|-------|------------|
| Framework | [CUSTOMIZE: e.g., Next.js 15] |
| Language | [CUSTOMIZE: e.g., TypeScript 5.x] |
| Database | [CUSTOMIZE: e.g., Supabase/Postgres] |
| Auth | [CUSTOMIZE: e.g., Supabase Auth] |
| Hosting | [CUSTOMIZE: e.g., Vercel] |
| Styling | [CUSTOMIZE: e.g., Tailwind + shadcn/ui] |

---

*This project follows The FORGE Method(TM) — theforgemethod.org*
