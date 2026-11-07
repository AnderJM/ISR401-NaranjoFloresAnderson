# Ingeniería de Requerimientos (ISR-401)

Repositorio personal de **Anderson Jeampiere Naranjo Flores**, estudiante de Ingeniería de Software de la Universidad Técnica Estatal de Quevedo.

**Docente:** PhD. Gleiston Cicerón Guerrero Ulloa  
**Nivel y paralelo:** Cuarto nivel, Software A

## FORM-TL-01: Identificación y clasificación de tipos de requisitos

**Caso de estudio:** Plataforma de gestión de citas médicas del Policlínico Ribera del Quevedo, organización ficticia descrita en el material del docente.

El documento contiene:

- Clasificación de los 20 enunciados en las dimensiones tipo de requisito, producto o proceso y sistema o software.
- Características y subcaracterísticas de ISO/IEC 25010:2023 para los requisitos de calidad.
- Justificación de cada clasificación.
- Reformulación de cinco requisitos vagos mediante métricas, umbrales y condiciones de verificación.
- Identificación de problemas de ambigüedad y falta de verificabilidad.
- Comparación documental de los criterios visibles en un fragmento del trabajo de David Octavio Vaca Romero.
- Referencias y declaración del uso de herramientas de apoyo.

Los umbrales planteados son propuestas de aceptación. No representan mediciones realizadas ni acuerdos con los interesados del caso.

## Estructura de archivos

```text
FRM-TL-01/
├── main.tex
├── referencias.bib
├── main.pdf
├── portada_sga.tex
└── portada_sga.pdf

README.md
```

- `main.tex`: documento principal con la clasificación, las reformulaciones, la comparación y los enunciados originales.
- `referencias.bib`: bibliografía utilizada por el documento.
- `main.pdf`: informe académico compilado.
- `portada_sga.tex`: fuente de la portada informativa.
- `portada_sga.pdf`: portada de una página destinada al SGA.

El documento principal está contenido en un solo archivo `.tex`. No requiere una carpeta de secciones ni archivos de imágenes.

## Requisitos de compilación

**Compilador:** XeLaTeX.  
**Gestor de bibliografía:** BibTeX.  
**Estilo bibliográfico:** IEEEtran.

Se puede utilizar TeX Live o MiKTeX, junto con Visual Studio Code y la extensión LaTeX Workshop.

Paquetes utilizados:

- `fontspec`
- `babel`, con soporte para español
- `geometry`
- `array`
- `booktabs`
- `longtable`
- `tabularx`
- `enumitem`
- `microtype`
- `fancyhdr`
- `hyperref`

También se necesita la fuente **Latin Modern Roman** y el archivo de estilo bibliográfico **IEEEtran.bst**.

## Compilar el documento principal

Desde la raíz del repositorio, abrir una terminal y ejecutar:

```bash
cd FRM-TL-01
xelatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
xelatex -interaction=nonstopmode -halt-on-error main.tex
xelatex -interaction=nonstopmode -halt-on-error main.tex
```

BibTeX procesa `referencias.bib`. Las dos ejecuciones posteriores de XeLaTeX incorporan la bibliografía y actualizan las citas.

El resultado se genera como `FRM-TL-01/main.pdf`.

Después de modificar el documento o sus referencias, se debe repetir la compilación y actualizar el PDF publicado.

## Compilar la portada del SGA

Desde la carpeta `FRM-TL-01`, ejecutar:

```bash
xelatex -interaction=nonstopmode -halt-on-error portada_sga.tex
```

El resultado se genera como `portada_sga.pdf`.

La portada debe mostrar los datos del estudiante, el código y nombre de la actividad, la fecha límite y la URL completa del repositorio en una sola línea.

## Compilar en Overleaf

1. Crear un proyecto y subir `main.tex` y `referencias.bib`.
2. Seleccionar **XeLaTeX** como compilador.
3. Establecer `main.tex` como documento principal.
4. Compilar y descargar el PDF.
5. Guardar el resultado como `FRM-TL-01/main.pdf`.

Para generar la portada, subir `portada_sga.tex`, seleccionarlo como documento principal y compilarlo también con XeLaTeX.

## Referencias utilizadas

La clasificación se apoya en el glosario de IREB y en las referencias normativas ISO/IEC/IEEE 29148:2018 e ISO/IEC 25010:2023.

También se utilizan los siguientes artículos para apoyar el análisis de calidad de los enunciados:

- Femmer y colaboradores, *Rapid quality assurance with Requirements Smells*, 2017.
- Montgomery y colaboradores, *Empirical research on requirements quality: a systematic mapping study*, 2022.

Los datos bibliográficos y enlaces están registrados en `referencias.bib`.

Los artículos respaldan el análisis de calidad de los requisitos. Los valores numéricos propuestos para el caso no se atribuyen a esas publicaciones.

## Comparación documental

Se revisó un fragmento del documento de **David Octavio Vaca Romero** compartido para esta actividad.

El contraste se limita a los criterios visibles sobre:

- E02 y la frontera entre sistema y software.
- E09 como requisito funcional derivado de una regla del dominio.
- La interpretación de sistema/software en los requisitos de proceso.

No se dispone de la matriz completa del compañero. Esta revisión documental no demuestra una conversación ni un acuerdo bilateral.

Si se realiza una discusión posterior, se registrarán su fecha, los argumentos de ambos y los acuerdos o diferencias que realmente se mantengan.

## Uso de herramientas de apoyo

Se utilizó ChatGPT de OpenAI como apoyo para preparar propuestas de clasificación, formular métricas, organizar el documento en LaTeX y revisar su compilación.

El documento declara ese apoyo. La revisión del contenido y la capacidad de explicar las decisiones corresponden al estudiante.

No se presentan pruebas de campo, resultados de evaluación ni acuerdos con compañeros que no se hayan realizado.

## Revisión antes de entregar

1. Revisar las 20 clasificaciones y sus justificaciones.
2. Comprobar las características y subcaracterísticas de calidad utilizadas.
3. Revisar que los cinco requisitos reformulados tengan métricas, unidades, umbrales y condiciones verificables.
4. Completar la discusión real con el compañero cuando se realice.
5. Comprobar que las citas aparezcan correctamente y que no existan referencias marcadas con signos de interrogación.
6. Regenerar `main.pdf` después de la última modificación.
7. Publicar los fuentes y el PDF actualizado en el repositorio.
8. Comprobar que el repositorio pueda abrirse sin iniciar sesión.
9. Verificar que `portada_sga.pdf` tenga exactamente una página y que su enlace funcione.

## Entrega en el SGA

Subir únicamente **`FRM-TL-01/portada_sga.pdf`**.

El informe completo y sus fuentes se conservan en este repositorio.

**Fecha límite confirmada para esta entrega:** 7 de noviembre de 2026, a las 23:59, hora de Ecuador.

## Repositorio

https://github.com/AnderJM/ISR401-NaranjoFloresAnderson

Los commits deben describir cambios reales. El historial debe reflejar el trabajo efectivamente realizado.