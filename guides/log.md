# Logging — the 2-minute version

Read once after START.md. After that, you just do it.

"You are here": [README](../README.md) → [START](../START.md) → **log**

**This file's job:** how to fill in `PROGRESS.md` and `BACKLOG.md` in 2 minutes, with an example to copy. Session rhythm itself is [operation_manual.md](../operation_manual.md).

---

## 1. The rule

At the end of every session, update `PROGRESS.md`. Two minutes. Three small things:

1. **Now → Next:** write tomorrow's first step.
2. **Log:** add one short row.
3. **Done:** only when a milestone finishes.

That's it. If logging takes longer than 2 minutes, you are writing too much.

Why it exists: after a week away, you open `PROGRESS.md`, read **Next**, and start in 30 seconds. No archaeology.

## 2. `PROGRESS.md` — the three parts

Create it once:

```bash
cp PROGRESS.template.md PROGRESS.md
```

### Now — where you are

```markdown
## Now

- Milestone: 01 — Argument Inspector (Roadmap Week 1)
- Next: Print cwd in srcscope/src/main.cpp
- Stuck on: none
```

Rules for **Next** (the only line that matters):

- One step, with a file: *"Print cwd in srcscope/src/main.cpp"*.
- Never vague: *"work on M01"*, *"clean things up"* — bad. Tired future-you must be able to start without re-reading anything.
- Never blank at day's end. Even *"Run tests and commit"* counts.

**Stuck on** is `none` most days. When blocked, name what you need: *"linker error, see lost.md"*.

### Log — one row per session

```markdown
| Date       | Did                                  | Next                |
|:-----------|:-------------------------------------|:--------------------|
| 2026-10-23 | First build green; broke/fixed a test; started M01 | Print cwd in main.cpp |
```

One line. What shipped, then what's next. Details go nowhere — if it needs more than a line, it belongs in a commit message, not here.

### Done — only when a milestone finishes

```markdown
### M01 — Argument Inspector

- Finished: 2026-10-25
- Proof: ctest → 2/2 passed; commit b7f2d11 feat(srcscope): argument inspector (M01)
```

**Proof** = test result + commit. One line. If you can't name the commit, the milestone isn't done yet. This is what [checklist.md](../checklist.md) means by "tick only with evidence".

## 3. `BACKLOG.md` — ideas parking lot

Create it the first time an idea appears:

```bash
cp BACKLOG.template.md BACKLOG.md
```

One line per idea:

```markdown
- `--tree flag` — would help M03 tests; after M03.
```

Add it, keep coding on the milestone. Don't design it, don't estimate it, don't discuss it. A backlog item becomes work only when you move it into **Next** — that's the whole promotion process.

## 4. When to write — three moments

| Moment | Write |
|:-------|:------|
| End of every session (last 2 min) | **Now** (Next is never blank) + one **Log** row |
| Milestone finished | One **Done** block + commit |
| A good idea appears mid-work | One **BACKLOG.md** line, then back to work |

Weekly review and phase reviews ([operation_manual §5, §11](../operation_manual.md)) just re-read this file. No extra writing.

## 5. What NOT to do

- Don't copy acceptance criteria into PROGRESS.md. They live in the Roadmap.
- Don't record build commands or commit hashes every session. Commits already store that; **Done** blocks store the ones that matter.
- Don't write paragraphs. One line per thing.
- Don't skip it. A missing **Next** costs you 30+ minutes next session. Two minutes now saves that.

---

· **Related:** [START.md](../START.md) — your first entry · [lost.md](lost.md) — from "where was I?" to visible state
