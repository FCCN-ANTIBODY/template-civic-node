# Orientation

This repository is a **civic node**: one installation that can publish, direct,
collect, and keep. It coordinates engines as hidden submodules — `.journal-engine/`,
`.atlas-engine/`, `.tell-engine/`, `.antidote-engine/` — and supplies only content,
configuration, and declarations.

It is a template. The reference node it was stripped from is
[`civic-node`](https://github.com/FCCN-ANTIBODY/civic-node), which is also the
constellation's documentation home; its `VISION.md`, `OPEN-QUESTIONS.md` and `docs/`
are deliberately **not** copied here. Read them there.

## The roles are optional and self-declared

Each role announces itself at a fetchable path — `journal.yml` (synced from the
engine), `atlas.yml`, `antidote.yml`, and the Tell's own config. A directory reads
those rather than guessing from your name or your URL shape.

So: **delete the declarations for roles you do not run.** A role announced but not
filled is a false statement about what this node is, and the whole reason
declarations beat inference is that they can be trusted.

Roles are not exclusive. A node running three publishes three, and that is the
honest description of it.

## NAME, and why not CNAME

`NAME` is one line, no scheme: this node's claim about its canonical address.
Deliberately not `CNAME` — a CNAME asserts one host is an *alias* of another, and
canonical here means **a proven copy, not the only copy**. The same branch may be
mirrored to a different apex and be canonical at both.

Site-owned, so no engine sync touches it. Per-branch, so a repository serving
several places carries a different NAME on each branch — which makes the number of
branches the number of nodes, disclosed rather than inferred.

## Invariants — violate these and you are building the wrong system

1. **Neighbors, not a graph.** No central authority; one hop, no transitive reach.
2. **Verify-from-anyone; trust decides *action*, not *admission*.**
3. **Witness, not judge.** Never block a submission — the submitter learns the outcome.
4. **Sign ≠ decrypt.** Vouching for bytes and reading them are different powers.
5. **Honest defaults fire nothing.** Judges, thresholds, automation ship *off*.
6. **Attest before you run.** New conduct goes into `CONSTITUTION.md` in plain words
   before it is coded.
7. **Content-id is the join key.** Never a second hashing scheme.
8. **No new cryptography without cause.**

And the one that governs the rest: **replication is the test.** Would the next
operator be able to copy this and understand what they copied? You are that operator
right now — if something here is unclear, that is a defect worth reporting upstream.

## Things that look like harmless shortcuts and are not

- **Do not shallow-clone.** Per-paragraph history is generated into `_data/` at build
  time; history *is* the data model.
- **Do not edit engine-synced files.** Layouts, includes, css, and the skel pages are
  rewritten on every build. Change the engine, or shadow a file deliberately.
- **Do not charter the Antidote as a setup step.** It ships UNCHARTERED and admits
  nothing. Chartering is a deliberate act with a content hash behind it.
- **Do not put your address anywhere but `NAME`.** A second copy is a second truth.
