# CSE 4316/4317 Senior Design — Documentation Templates (2026 edition)

This folder is a modernization of the original `documentation/` templates. The
document structures were revised to follow the **current ISO/IEC/IEEE standards**
for each deliverable, replacing the withdrawn IEEE standards the originals were
based on.

## Standards mapping

| Template | Follows (current) | Replaces (withdrawn/legacy) |
|---|---|---|
| `project charter latex/` | ISO/IEC/IEEE **16326:2019** (project management), within 12207:2017 / 15288:2023 | IEEE 1058 |
| `system requirements specification LaTeX/` | ISO/IEC/IEEE **29148:2018** (requirements engineering) | IEEE 830-1998 |
| `architectural design specification latex/` | ISO/IEC/IEEE **42010:2022** (architecture description) + IEEE **1016-2009** | — |
| `detailed design specification latex/` | IEEE **1016-2009** (software design descriptions) | — |
| `test plan latex/` (new) | ISO/IEC/IEEE **29119-3:2021** (test documentation) | IEEE 829-2008 |
| `individual sprint report LaTeX/` | aligned with ISO/IEC/IEEE **26515:2018** (agile documentation) | — |

`ISO/IEC/IEEE 15289:2019` (content of life-cycle information items) and
`ISO/IEC 25010:2023` (SQuaRE product quality model) inform the requirement and
design content across the set.

## What changed

- **SRS** — reorganized to the 29148 SRS outline (Introduction / Product Overview,
  a Requirements Engineering Approach section, requirement groups by type, and a
  Verification & Traceability section). Every requirement now carries the 29148
  attribute set: Description, **Rationale**, Source, Priority, **Verification
  Method**, Constraints, Applicable Standards. Requirements use stable IDs.
- **ADS** — reframed as an ISO/IEC/IEEE 42010 architecture description:
  Stakeholders & Concerns, Architecture Viewpoints, views (the X/Y/Z layers),
  Architecture Decisions & Rationale, and Requirements Traceability.
- **DDS** — reframed as an IEEE 1016 Software Design Description: Design
  Stakeholders & Concerns, Design Viewpoints, and per-subsystem design organized
  by viewpoint (context, composition, information, interface, interaction/state,
  algorithm, resource), plus Requirements Traceability.
- **Project Charter** — added a Project Management Approach section (life cycle
  model, processes, estimation & measurement, change/configuration management)
  aligned with 16326.
- **Test Plan** — a new LaTeX template following 29119-3; the legacy IEEE 829
  materials are retained in `test plan/` for historical reference.
- **Sprint Report** — fixed the peer-review table column order to match the
  evaluation-item order (Participation, Communication, Work quality,
  Professionalism, Overall) and corrected invalid `\begin{item}` markup to `\item`.
- All `reference/refs.bib` files updated with current standards citations (master
  copy in `_shared/refs.bib`).

## `example/`

Four fully worked sample projects, one per domain, each carrying the full set of
modernized documents:

- `autonomous-ground-robot/` — embedded robotics platform (hardware + firmware + software)
- `computer-vision-ml/` — handwritten-digit recognition service (ML pipeline)
- `full-stack-web-app/` — a web data dashboard (frontend / backend / data tiers)
- `mobile-app-iot/` — a phone app paired with a Bluetooth sensor device

## Building the PDFs

No PDFs are checked in (they would be stale). Build any document with a LaTeX
toolchain, e.g. Overleaf, or locally:

```bash
pdflatex <document>.tex
bibtex   <document>
pdflatex <document>.tex
pdflatex <document>.tex
```
