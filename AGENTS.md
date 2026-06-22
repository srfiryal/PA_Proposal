# AGENTS.md — PRISM Thesis Proposal (LaTeX)

## Identity
- **Title:** Kerangka Kerja Berbasis AI untuk Otomatisasi Lapisan Data, Logika Bisnis, dan Struktur Antarmuka Pengguna dari Spesifikasi API Backend
- **Author:** Sarah Rizqi Firyal (NRP 3123600033)
- **Institution:** D4 Teknik Informatika, PENS
- **Language:** Bahasa Indonesia
- **Reference:** IEEE numeric, biblatex+biber

## Compilation
```bash
pdflatex -interaction=nonstopmode main.tex
biber main
pdflatex -interaction=nonstopmode main.tex
pdflatex -interaction=nonstopmode main.tex
```
Output: `main.pdf`

## File Map
| File | Purpose |
|---|---|
| `main.tex` | Master — packages, margins, includes |
| `cover.tex` | PENS cover page |
| `pengesahan.tex` | Inner cover + approval |
| `abstrak.tex` | Abstract (ID + EN) |
| `katapengantar.tex` | Foreword |
| `bab/bab1.tex` | Pendahuluan |
| `bab/bab2.tex` | Kajian Pustaka |
| `bab/bab3.tex` | Desain Sistem |
| `daftarpustaka.bib` | IEEE bibliography (biber) |
| `image/` | Logos and figures |

## Content Rules

### Approach
- PRISM = CLI code-gen framework, hybrid deterministic–LLM pipeline
- NOT multi-agent, NOT MCP server, NOT "skill"
- 7-stage orchestrated pipeline, not 4 "agent" stages
- Deterministic rules first (types, formats, enums, constraints, auth from OpenAPI)
- LLM only for ambiguous semantic interpretation + code repair

### Terminology
- `Presentation–Domain–Data` (selected by PRISM, not Flutter official recommendation)
- **Schema Reference Graph** (not Entity Relationship Graph)
- **Scaffolding** (not "scaffolding")
- **Feature module** / endpoint group as evaluation unit (not per-endpoint)

### State Management
- BLoC primary; Riverpod = future work only

### Numerical Claims
- All % and time values = targets/hypotheses, not established results
- Only cite numbers directly supported by sources

### References — IEEE, Biber
- All `\cite{key}` → numeric `[n]`
- Corrected from draft:
  - Removed [6] (AI Doc Generator — irrelevant)
  - [7] = classification accuracy, not build success
  - [14] = schema-driven prompting concept only, no token claims
  - [17] = OpenAPI Generator (separate from IntelliUnitGen)
  - [20] = replaced (unverifiable)
  - [22] = fixed authors (Otoum & Elkhalili)
  - [23] = fixed (LIBRO = bug reproduction)
  - [24] = replaced with empirical study
  - Merged [8]/[19] duplicates

### Write Protocol
- Edit `.tex` files directly, recompile after
- Never regenerate entire project
- Preserve LaTeX formatting
- Bahasa Indonesia, formal academic

## Git — Version-Based Branching
- Branch: `X.Y.Z` (semver)
- MAJOR = structural rewrite
- MINOR = section addition / major content
- PATCH = typos, ref fixes, wording
