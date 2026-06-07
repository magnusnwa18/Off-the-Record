# CLAUDE.md — *Midnight in Manchester*

> Project guidance for Claude Code. **Read this first, every session, before writing or revising any prose.**

This repository is a novel: **_Midnight in Manchester_** — a dual-POV new-adult romance (Off-Campus energy, moody British aesthetic) set against elite university life in Manchester and the city's underground music scene. Heroine **Eleonora "Ella" Savage-Oluwa** (21, stylist/creative director); hero **Callum "Cal" Vance** (22, academy fly-half secretly ghost-producing as "V").

> **This book was produced with a reusable system: see [`framework/`](framework/README.md) — "The Novel Engine".** It captures the repeatable method (spec → architecture → bible → plan → draft → revise) and the quality rules used to build this novel. To start a *different* book of the same quality, copy `framework/STORY-SPEC.template.md`, fill it in, and follow `framework/METHOD.md` (or run `framework/scaffold.sh` to spin up a fresh project). `framework/STORY-SPEC.example.md` shows this novel's spec as a worked reference.

---

## ⚑ Use these skills (mandatory)

A book-writing toolkit lives in **`.claude/skills/`**. Load and apply the relevant ones for every task — do not write fiction for this project without them in context:

| Skill | Use it for |
|-------|-----------|
| **structure-storyteller** | Architecture: outlines, beats, pacing, causality (because/therefore/but), character arcs, theme-as-argument, plot-hole checks. Use *before* drafting a new chapter and *before* any restructure. |
| **prose-craftsman** | Line-level craft: voice, rhythm, dialogue subtext, cutting filtering/flab. **Prime directive: sharpen the established voice, never replace it.** |
| **continuity-keeper** | The canonical ledger. **`STORY-BIBLE.md` is the source of truth.** Check names, ages, timeline, and "who-knows-what-when" against it; update it when canon changes; flag retcons. |
| **project-manager** | Schedule + word-count tracking. **`PRODUCTION-PLAN.md` is the live tracker.** Update it every pass; report pace honestly. |
| **revision-partner** | Process across sessions. Orient to the current **stage** (draft vs. revise vs. polish), recover context before acting, carry decisions forward, run one-focus revision passes. |
| **motivation-coach** | When stuck/blocked: diagnose the block, shrink the next action, protect momentum. |
| **research-integrator** | Authenticity: Manchester geography, rugby (fly-half craft, academy/scout pipeline), UK ghost-producer culture. Verify facts that matter; weave them in via POV, never info-dump. |

**Stage right now:** *Drafting* the long-form (per `PRODUCTION-PLAN.md`). Protect forward momentum; keep a "fix later" list rather than polishing mid-draft. Switch to revising only when a chapter hits length.

---

## Repository map

- **`chapters-long/`** — the real book: **5 long chapters, ~45,000 words each (~225k total)**, built progressively. Scenes are marked with `◆`.
- **`chapters/`** — the complete ~38k short-form draft (all 19 beats). This is the **locked scene skeleton / source material** the long chapters expand from. Don't delete; mine it.
- **`OUTLINE.md`** — logline, characters, the 5-chapter structure, themes, recurring motifs.
- **`STORY-BIBLE.md`** — continuity ledger (characters, places, timeline, information-state, threads, voice rules, open items to lock).
- **`PRODUCTION-PLAN.md`** — word-count tracker, pace projection, next action.

---

## Working rules for this project

1. **Voice is sacred.** Dual close-third, past tense. Ella = sharp, perceptive, self-aware about performing strength. Cal = controlled surface over a furnace; sport and production metaphors fuse. Long rhythmic sentences punctuated by short punches; British register; Manchester texture. Match it; don't flatten it.
2. **Honour the motifs** (see `OUTLINE.md`): the nod • the counting stillness • reading rooms/odds • "the catch can have everything else" • crossing the room • six o'clock • "off the record" • **Jordan's four notes (three climb, one falls)** buried in every track • looking away first = an apology • orange streetlight / "beautiful and slightly ruined" • both names spelled right. Use deliberately; flag overuse.
3. **No padding.** Expand only with scenes that earn their place (new interiority, dialogue, plot, texture). If a chapter is short of its 45k target, add *story*, not filler.
4. **Continuity first.** Before writing, reconcile against `STORY-BIBLE.md`. Never let a character act on knowledge before they learn it (the information-state ledger).
5. **Commit + push every pass** to the working branch so progress is visible and never lost. Update `PRODUCTION-PLAN.md` each time.

## Working branch & git
- Develop on **`claude/tender-feynman-SqN9U`**. Create locally if missing.
- `git push -u origin claude/tender-feynman-SqN9U`; retry on network errors (2s/4s/8s/16s).
- Do **not** open a PR unless explicitly asked.

## Chapter length policy (author decision, current — UPDATED)
**Target ~45,000 words per chapter.** Earlier chapters tapered (30k→14k→7k); the fix is to **grow each chapter to target by weaving in the B-plots** (see `STORY-BIBLE.md` → SUBPLOTS), NOT by padding the main scenes. Every added scene must (a) advance a subplot, (b) rhyme with the theme (authenticity vs. performance), and (c) not contradict or dilute the main A-story. Order of work: bring Ch.2 and Ch.3 up to ~45k via subplot scenes, top Ch.1, **then** draft Ch.4.

The three woven B-plots: **(1) Priya & Tom** (the honest mirror; the V-sweepstake irony), **(2) the degree show & Margot Hale** (Ella's professional stakes), **(3) Knox's commercial-feature temptation** (authenticity in the music world).

## Current status — FULL DRAFT COMPLETE ✅
All **5 long chapters drafted, every one ≥15,000 words** (`chapters-long/01–05`). Total ≈ 94,500 words. The novel runs end-to-end and closes with the Parklife epilogue ("THE END"). Main arc + all three B-plots resolved.

**Stage now → REVISE** (per revision-partner: switch from drafting to revising). Recommended next passes, cheap on tokens, one focus each:
1. Continuity/polish read against `STORY-BIBLE.md` (catch any drift; confirm information-state).
2. Even out chapter lengths if desired — Ch.2/3/4/5 sit ~15–18k, Ch.1 ~30k; either grow the others or trim Ch.1 for balance.
3. prose-craftsman line-polish pass, one chapter at a time.
Do NOT re-draft; the story is whole. Protect it; refine it.
