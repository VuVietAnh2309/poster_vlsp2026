# Poster: AI_TLfanclub at VLSP 2026 ViTNumChart

A1 portrait poster for the paper *Voting over Fine-Tuned Small Multimodal Program Writers, with an Analysis of Single-Writer Errors*.

## Build

Requires TeX Live (XeLaTeX) with the Fira fonts (`fira`, `firamath`), `pgfplots` and `baposter` dependencies.

```sh
latexmk -xelatex poster.tex   # produces poster.pdf
latexmk -c                    # remove build artefacts
```

Overleaf: set the compiler to **XeLaTeX**.

## Layout

| Path | Content |
|---|---|
| `poster.tex` | Main file: preamble, colours, all text boxes |
| `baposter.cls` | Poster class; `\baposter@fontscale` set to 0.58 (smaller value = larger text) |
| `figures/*.tex` | One TikZ/pgfplots figure per file, drawn from the paper's numbers |
| `logos/` | HUST and VLSP 2026 logos |
| `poster.pdf` | Last built version, for quick viewing |

To replace a figure with an image file, change its `\input{figures/...}` line in `poster.tex` to `\includegraphics[width=\linewidth]{...}`.

## Style

One accent colour (`accent`, HUST red) plus greys; section headers are bold text over a thin red rule; no icons. Check that the poster still fits on one page after editing (`pdfinfo poster.pdf` should report 1 page).
