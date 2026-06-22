# Proposal Proyek Akhir — PRISM

**Kerangka Kerja Berbasis AI untuk Otomatisasi Lapisan Data, Logika Bisnis, dan Struktur Antarmuka Pengguna dari Spesifikasi API Backend**

Sarah Rizqi Firyal (3123600033) — D4 Teknik Informatika, PENS

## Ringkasan

PRISM (*Pipeline for Rapid Intelligent Scaffolding of Mobile features*) adalah kerangka kerja CLI berbasis Python yang mentransformasikan spesifikasi OpenAPI menjadi modul fitur Flutter melalui pipeline hibrida deterministik–LLM.

## Kompilasi

```bash
pdflatex -interaction=nonstopmode main.tex
biber main
pdflatex -interaction=nonstopmode main.tex
pdflatex -interaction=nonstopmode main.tex
```

Prasyarat: TeX Live, biber.

## Struktur

```
.
├── main.tex              # Dokumen master
├── cover.tex             # Sampul PENS
├── pengesahan.tex        # Lembar pengesahan
├── abstrak.tex           # Abstrak (ID + EN)
├── katapengantar.tex     # Kata pengantar
├── daftarpustaka.bib     # Referensi IEEE
├── image/                # Logo dan gambar
└── bab/
    ├── bab1.tex          # Pendahuluan
    ├── bab2.tex          # Kajian Pustaka
    └── bab3.tex          # Desain Sistem
```
