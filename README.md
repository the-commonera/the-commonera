<div align="center">

# ◈ COMMONERA

### The Agent Specification Layer

`AGENT INFRASTRUCTURE` · `PACKAGING` · `VERSIONING` · `REPRODUCIBILITY` · `LEAST PRIVILEGE`

<br />

> **Agents shouldn't be hand-patched software.**
>
> They should be **defined, packaged, versioned, reproduced, composed, and distributed.**

<br />

![CommonEra](https://capsule-render.vercel.app/api?type=waving\&color=0:0F766E,50:2DD4BF,100:050708\&height=180\&section=header\&text=COMMONERA\&fontSize=42\&fontColor=CFFAFA\&animation=fadeIn)

</div>

---

## `01` — NO MORE DRIFT

> **Hand-patched agents silently diverge from what they originally were.**

Hand-patched agents silently diverge from what they originally were, one edit at a time, until nobody can say what the agent actually does anymore.

A spec-derived agent is always exactly what its spec says; there's no "it used to do X but someone tweaked it" ambiguity.

---

## `02` — DETERMINISTIC UPGRADES

> **Instead of manual patching.**

Change a requirement, bump the version, and the whole agent regenerates from scratch.

No hunting through files to find what needs editing; the classic "if I touch this, will something else quietly break" fear disappears.

---

## `03` — REPRODUCIBILITY

> **You always know exactly which version produced which result.**

Every output can be traced to a specific, pinned spec version, the same way a bug report traces to a specific software build.

That's audit-trail-grade accountability most agent tooling today can't offer.

---

## `04` — LEAST PRIVILEGE

### **By construction, not by discipline.**

> An agent scoped to `github_repo_file_push` cannot also push code or create repos.

Not because someone remembered to restrict it, but because it structurally doesn't have that capability.

This directly maps to the exact governance gap the industry names as its biggest 2026 security problem, agents accidentally or maliciously given more access than they need.

---

## `05` — COMPOSABILITY

> **Composability without collision.**

Because each primitive does exactly one scoped thing, you can safely combine many of them into a larger agent (Applied, something we are testing) without one primitive's access silently overlapping or conflicting with another's, the same reasoning that makes small, single-purpose functions safer to compose than one giant function.

---

## `06` — ROLLBACK

> **Rollback, for free.**

Since every version is a discrete, regenerable artefact, reverting a bad change is "reusing the previous spec version", not "try to remember and manually undo whatever I changed".

---

## `07` — REGISTRY

> **Turns tribal knowledge into a reusable asset.**

Instead of every team hand-building their own agent from scratch, a working, versioned spec gets published once and installed everywhere, the same leverage npm gives software, just applied to agents instead of code.

---

## `08` — BLAST-RADIUS CONTAINMENT

> **When something goes wrong.**

If a spec-derived agent misbehaves, the damage is capped by whatever single tool that primitive touches, not the entire surface area the underlying agent could theoretically reach.

---

<div align="center">

### `SPEC → PACKAGE → VERSION → REPRODUCE → COMPOSE → DISTRIBUTE`

<br />

`COMMONERA`

**The infrastructure layer for agents.**

<br />

![GitHub](https://img.shields.io/badge/AGENT_SPECIFICATION-0F766E?style=for-the-badge\&logo=github\&logoColor=white)
![Packaging](https://img.shields.io/badge/PACKAGING-050708?style=for-the-badge)
![Versioning](https://img.shields.io/badge/VERSIONING-050708?style=for-the-badge)
![Reproducibility](https://img.shields.io/badge/REPRODUCIBILITY-050708?style=for-the-badge)
![Least Privilege](https://img.shields.io/badge/LEAST_PRIVILEGE-2DD4BF?style=for-the-badge)

</div>

