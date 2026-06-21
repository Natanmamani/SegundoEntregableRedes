# Segundo Entregable - Redes I

Documento LaTeX del segundo entregable del curso **Redes I** (UNSAAC).

## Estructura

- `main.tex` — documento principal.
- `Estilo.sty` — paquete de estilo.
- `contenido/` — capítulos y secciones (`.tex`) y bibliografía (`bibliog.bib`).
- `images/` — figuras e imágenes.

## Compilación

```bash
latexmk -pdf main.tex
```

o de forma manual:

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```
