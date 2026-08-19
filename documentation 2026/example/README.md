# Worked examples

Four fully worked sample senior-design projects, one per domain, each carrying the
full set of modernized documents (Project Charter, SRS, ADS, DDS, and an individual
Sprint Report). They demonstrate how a real project fills in the 2026 templates and
follows the current standards end to end, including a consistent requirement-ID
scheme (`FR-01`, `PE-02`, …) traced from the SRS through the ADS and DDS.

| Folder | Project | Exercises |
|---|---|---|
| `autonomous-ground-robot/` | *TerraScout* PV-field inspection rover | embedded HW + firmware + autonomy + CV; safety |
| `computer-vision-ml/` | *DigitDesk* handwritten-form digitization | ML pipeline, calibration, human-in-the-loop, on-prem privacy |
| `full-stack-web-app/` | *CivicPulse* service-request dashboard | three-tier web, SSO/RBAC, geospatial, accessibility |
| `mobile-app-iot/` | *AquaGuard* smart leak monitor | BLE device + firmware + cross-platform app + cloud push |

Each document is a **self-contained** `.tex` file (its LaTeX preamble is inline, so
no shared template files are needed) and references the `images/` and `reference/`
folders inside its project directory.

## Building

No PDFs are committed. Build any document with a LaTeX toolchain (Overleaf, or a
local install):

```bash
pdflatex system_requirements_specification.tex
bibtex   system_requirements_specification
pdflatex system_requirements_specification.tex
pdflatex system_requirements_specification.tex
```

The figures are the generic placeholder diagrams inherited from the templates
(`test_image`, `layers`, `subsystem`, `data_flow`); a real team would replace them
with project-specific diagrams.
