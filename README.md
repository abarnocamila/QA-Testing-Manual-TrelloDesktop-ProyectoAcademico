# Testing Manual sobre Trello Desktop - Proyecto realizado como parte del curso Tester QA – Testing Para Todos. 

## Propósito
Es un proyecto de testing manual que hice sobre la app de escritorio de Trello como parte de mi capacitación como QA. La idea fue trabajar como si fuera un entorno real, con requerimientos, herramientas de la industria y documentación formal.

Las funcionalidades que elegí testear fueron la creación de tableros y la creación de tarjetas dentro de un tablero, cubriendo tanto los flujos esperados como los que tuvieron resultados negativos.

## Contenido del repo

* README.md - Este archivo
* TEST-PLAN.pdf - Plan de pruebas

docs/
* Análisis-funcional.pdf - Análisis de requerimientos y mapa mental
* casos-de-prueba.csv - Los 22 casos con su resultado de ejecución
* Bugs-identificados.csv - Reporte de los bugs encontrados

Img-importadas-en-tablas/ - Capturas de evidencia de cada bug
* BUG-01-Caracteres-InvisiblesTrello.png
* BUG-02-Caracteres-Invisibles-Tarjetas-Trello.png

Evidencias/
* Evidencia-de-herramientas-utilizadas.pdf

## Resumen del alcance

Funcionalidades cubiertas:
Creación de tablero - Flujo completo: desde abrir el modal hasta confirmar la creación, con distintas configuraciones de nombre, visibilidad y espacio de trabajo
Creación de tarjetas - Inputs válidos e inválidos, persistencia de datos y comportamiento visual

Los tipos de prueba que incluí fueron escenarios positivos y negativos, validación de inputs (campos vacíos, espacios, caracteres especiales, caracteres invisibles y límite de caracteres), persistencia de datos, comportamiento de la interfaz y un caso de error de red.

## Flujo que se siguió en el proyecto

Análisis funcional → Diseño de casos → Ejecución → Reporte de bugs → Documentación

1. Análisis funcional — Identifiqué los flujos principales y alternativos, y definí qué iba a cubrir y qué no.
2. Diseño de casos de prueba — Diseñé 22 casos entre positivos, negativos y de error.
3. Ejecución — Ejecuté todos los casos en Jira con Zephyr Scale.
4. Reporte de bugs — Documenté los 2 defectos encontrados con pasos para reproducirlos y capturas de evidencia.
5. Documentación — Utilicé Confluence además de dejar la documentación en este proyecto de GitHub.

## Resultados

Casos de prueba diseñados: 22
Casos ejecutados: 22
Pasaron: 20
Fallaron: 2
Bugs reportados: 2 

## Herramientas que usé

Trello Desktop: App que estuve testeando
Jira + Zephyr Scale:  Gestión y ejecución de los casos de prueba
Confluence:  Documentación del proyecto
MindMeister: Mapa mental del análisis funcional
Notion: Notas y documentación inicial
Git + GitHub: Control de versiones

## Artefactos

- [Plan de pruebas](test_plan.pdf)
- [Análisis funcional](docs/Análisis_Funcional.pdf)
- [Casos de prueba](docs/casos-de-prueba.csv)
- [Bugs reportados](docs/Bugs-identificados.csv)
- [Evidencia de herramientas](Evidencias/Evidencia-de-herramientas-utilizadas.pdf)

## Bugs encontrados

### BUG-01 — El campo "Nombre" acepta caracteres invisibles al crear un tablero
- **Severidad:** Baja
- **Prioridad:** Media
- **Estado:** Abierto
- Al ingresar únicamente caracteres invisibles en el campo Nombre, el sistema habilita el botón Crear y genera un tablero que aparece sin nombre. Debería validar que el campo tenga contenido visible.
- Caso relacionado: CP-14

### BUG-02 — Se puede crear una tarjeta con caracteres invisibles
- **Severidad:** Baja
- **Prioridad:** Media
- **Estado:** Abierto
- El mismo problema pero en la creación de tarjetas: si se ingresan solo caracteres invisibles, la tarjeta se crea y queda visualmente vacía en el tablero.
- Caso relacionado: CP-22

## Aprendizajes del proyecto

Fue un buen ejercicio para practicar el ciclo completo de testing desde cero. Lo que más me aportó fue aprender a pensar en los casos menos obvios (como los caracteres invisibles, que no es algo que uno prueba por instinto), documentar defectos de forma clara y reproducible, y usar Jira + Zephyr de manera integrada para gestionar la ejecución.
