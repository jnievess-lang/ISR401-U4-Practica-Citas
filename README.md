
# Prueba Práctica — Unidad IV · Paralelo B

**Ingeniería de Requisitos (ISR-401)**
Universidad Técnica Estatal de Quevedo · Facultad de Ciencias de la Ingeniería
Carrera de Ingeniería de Software · Docente: Ing. Gleiston Guerrero, Mg.

**Estudiante:** Nieves Sánchez Jimmy Samuel — 4.º Software "B"
**Caso:** Sistema de Reserva de Citas Médicas

---

## Contenido del repositorio

```
.
├── main.tex          # Archivo principal: plantilla original del docente
│                       (inalterada) + \input{respuestas} al final
├── respuestas.tex     # Desarrollo de las actividades prácticas (P1–P10)
├── referencias.bib   # Base bibliográfica (6 entradas citadas con \citep)
├── main.pdf          # PDF compilado
├── figuras/          # Capturas del cuestionario del SGA (no los diagramas:
│                       P1, P2 y P3 están en TikZ dentro de respuestas.tex)
│   ├── sga_resumen.png
│   └── sga_evaluacion.png
├── .gitignore        # Excluye archivos auxiliares de LaTeX
└── README.md         # Este archivo
```

## Compilador

**pdflatex** (TeX Live 2023 o superior / MiKTeX). El documento usa `natbib` +
BibTeX, por lo que se requiere el ciclo completo de cuatro pasadas.

## Orden exacto de comandos

```bash
git clone <URL_DEL_REPOSITORIO>
cd <carpeta_del_repositorio>

pdflatex main.tex
bibtex   main
pdflatex main.tex
pdflatex main.tex
```

- **Archivo principal:** `main.tex`
- **Salida:** `main.pdf`

Si se omite `bibtex` o las dos pasadas finales, las citas aparecen como `[?]` y
la sección *Referencias* queda vacía.

## Dependencias (paquetes LaTeX)

`inputenc` (utf8), `fontenc` (T1), `helvet`, `textcomp`, `geometry`, `amsmath`,
`amssymb`, `graphicx`, `xcolor` (opciones `table`, `dvipsnames`), `array`,
`tabularx`, `multirow`, `colortbl`, `booktabs`, `enumitem`, `microtype`,
`parskip`, `titlesec`, `fancyhdr`, `caption`, `pdflscape`, `natbib`
(opciones `numbers`, `sort&compress`), `hyperref`, `tcolorbox` (opción `most`),
`tikz`.

Con una instalación completa (`texlive-full` o MiKTeX) no hace falta instalar nada.
En Debian/Ubuntu con instalación mínima:

```bash
sudo apt-get install texlive-latex-base texlive-latex-recommended \
     texlive-latex-extra texlive-pictures texlive-fonts-recommended \
     texlive-bibtex-extra lmodern
```

## Notas

- La plantilla original del docente se conserva sin modificaciones. El desarrollo
  de las actividades comienza después de un `\clearpage`, en la sección
  **DESARROLLO DE LAS ACTIVIDADES PRÁCTICAS**.
- Los diagramas UML (P1, P2, P3) están elaborados en TikZ dentro de
  `respuestas.tex`; no se requieren archivos externos para reproducirlos.
- Las capturas del cuestionario del SGA se incluyen en la carátula desde
  `figuras/`.

