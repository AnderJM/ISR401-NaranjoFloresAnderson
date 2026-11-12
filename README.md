# Ingeniería de Requerimientos (ISR-401)

Repositorio personal de **Anderson Jeampiere Naranjo Flores**, estudiante de Ingeniería de Software de la Universidad Técnica Estatal de Quevedo.

**Docente:** PhD. Gleiston Cicerón Guerrero Ulloa  
**Nivel y paralelo:** Cuarto nivel, Software A

En este repositorio se publicarán las **tareas individuales de Ingeniería de Requerimientos**, incluidas las actividades formativas. Cada actividad tendrá su propia carpeta con el informe en PDF, los archivos fuente y los recursos necesarios para compilarlo.

## Actividades

1. **[FORM-TL-01 — Identificación y clasificación de tipos de requisitos](./FRM-TL-01/)**  
   Actividad formativa sobre la plataforma de citas médicas del Policlínico Ribera del Quevedo. Incluye la clasificación y justificación de 20 enunciados, la reformulación de cinco requisitos y un contraste documental con el trabajo de un compañero.

2. **[TA-IND-01 — IEEE 29148 y tipos de requisitos de un sistema conocido](./TA-IND-01/)**  
   Trabajo individual sobre Instagram para Android. Incluye un resumen analítico de ISO/IEC/IEEE 29148:2018, un glosario de diez términos, 15 requisitos de cinco tipos, criterios de aceptación, una autoevaluación y tres capturas propias. Cinco requisitos de calidad se clasifican según ISO/IEC 25010:2023 e incluyen métricas y umbrales propuestos.

## Estructura del repositorio

```text
.
├── README.md
├── FRM-TL-01/
│   ├── main.tex
│   ├── referencias.bib
│   ├── main.pdf
│   ├── portada_sga.tex
│   └── portada_sga.pdf
└── TA-IND-01/
    ├── README.md
    ├── main.tex
    ├── referencias.bib
    ├── main.pdf
    └── figuras/
        ├── F01.png
        ├── F02.png
        └── F03.png
```

## Compilación

Se requiere **XeLaTeX**, **BibTeX** y la fuente **Latin Modern Roman**. Cada informe carga su propia bibliografía. La formativa usa `IEEEtran.bst` y el trabajo individual usa `ieeetr.bst`.

Desde la raíz del repositorio, entra a la carpeta de la actividad correspondiente y ejecuta:

```bash
cd TA-IND-01
xelatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
xelatex -interaction=nonstopmode -halt-on-error main.tex
xelatex -interaction=nonstopmode -halt-on-error main.tex
```

Para compilar la formativa, usa `cd FRM-TL-01` desde la raíz. En ambos casos, el resultado es `main.pdf` dentro de la carpeta de la actividad.

## Entrega en el SGA

El informe y sus fuentes se publican en este repositorio. Para cada actividad, al SGA se sube únicamente la **portada informativa de una página**, con la URL completa del repositorio en una sola línea.

## Evidencias y herramientas de apoyo

Las capturas de Instagram documentan las pantallas observadas. Los umbrales de calidad son propuestas de aceptación y las pruebas se registran cuando se ejecutan. El contraste de la formativa se basa en un fragmento del trabajo de un compañero.

En los informes se declara el uso de ChatGPT como apoyo para organizar el contenido, revisar los requisitos y preparar los archivos LaTeX.
