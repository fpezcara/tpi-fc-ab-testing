# TPI Organización Empresarial: A/B Testing en Funding Circle

Trabajo Práctico Integrador de Organización Empresarial (Tecnicatura Universitaria en Programación a Distancia, UTN).

## Descripción del sistema

Funding Circle es una plataforma que conecta a pequeñas y medianas empresas (PyMEs) que necesitan financiamiento con inversores. Este proyecto propone un módulo de A/B Testing con PostHog para la página de solicitud de préstamos. El módulo muestra a cada visitante el formulario actual (control) o uno simplificado (test) y registra, por cada visita, si se envió la solicitud o no (conversión). Así el área de producto puede decidir con datos qué diseño conviene, sin descuidar la tasa de aprobación de las solicitudes.

Meta principal: aumentar al menos un 8% la tasa de conversión de la página de solicitud respecto de la línea base, medida durante las primeras 4 semanas del experimento.

## Integrante

- Florencia Pezcara

## Enlaces

- Repositorio: https://github.com/fpezcara/tpi-fc-ab-testing
- Tablero de gestión (GitHub Projects): https://github.com/users/fpezcara/projects/2

## Contenido del repositorio

| Carpeta | Contenido |
| --- | --- |
| `entregas/entrega_1/` | Caso Funding Circle, enfoque sistémico e interdependencia de módulos |
| `entregas/entrega_2/` | FODA, objetivo y metas, diagrama de Gantt |
| `entregas/entrega_3/` | Organigramas y diccionario de datos |
| `entregas/entrega_4/` | Diagrama BPMN, indicadores de control y PDF final consolidado |

## Historias de usuario

Cada historia es un issue del repositorio y se sigue en el tablero con los estados Por hacer, En Progreso y Listo.

1. Como Product Manager, quiero configurar un experimento que reparta el tráfico de la página de solicitud entre la variante control y la variante test, para comparar el diseño actual con el nuevo sin exponer a todos los solicitantes.
2. Como dueña o dueño de una PyME, quiero completar la solicitud de préstamo en un formulario más simple, para pedir financiamiento en menos tiempo.
3. Como Underwriter, quiero comparar la tasa de aprobación de las solicitudes de cada variante, para asegurar que el nuevo diseño no atraiga solicitudes de peor calidad.

Las historias siguen En Progreso hasta cumplir sus criterios de aceptación, porque el proyecto va del 5/10 al 18/12 según el Gantt de la Entrega 2. En esta etapa se completó la documentación de cada una (diagrama BPMN, indicadores de control y README), cargada como sub-issue de la historia y cerrada por su Pull Request.

## Forma de trabajo con Git

Después del commit inicial, cada cambio se hizo en una rama secundaria y entró a `main` por Pull Request. La revisión de los Pull Requests la hizo la propia autora, porque el trabajo es individual, siguiendo la indicación de la cátedra en el foro. Cada PR describe el cambio, y los de la Entrega 4 referencian su issue. En el PR del diagrama BPMN (#5) y en el del README, la revisión quedó en un checklist en la descripción y en comentarios sobre las líneas revisadas.

## Declaración de Uso de IA

Usé un asistente de IA (Claude) para estructurar cada entrega a partir de la consigna, proponer borradores y pulir la redacción. Le pasé al asistente la consigna de cada entrega y los apuntes de la cátedra, para que las respuestas usaran los conceptos de la materia. Tomé cada respuesta como un borrador a verificar, y las decisiones finales son mías.

| Uso | Prompt representativo | Corrección propia |
| --- | --- | --- |
| Organigramas | "Leé la consigna de la entrega 3 y el apunte de organigramas y proponeme cómo encararla para mi caso." | Puse Producto y Diseño bajo el CTO, porque en mi caso no hay CPO, y redibujé los organigramas según la norma IRAM. |
| Diccionario de datos | "Proponé entidades y campos para el módulo de A/B testing." | Saqué la entidad PyME y el consentimiento, porque no hacían falta para medir la conversión (minimización de datos). |
| BPMN | "Armame un borrador BPMN del proceso de solicitud con pools y lanes según el apunte." | Saqué pasos que el experimento no cambia (validación y registro del abandono) y agrupé la evaluación crediticia en un subproceso, porque tiene otro dueño. |
| Historias de usuario | "Proponeme tres historias de usuario con criterios de aceptación para el módulo." | Saqué criterios técnicos, como la latencia de PostHog, y dejé solo lo nuevo de cada historia. |
| Indicadores de control | "Armá una tabla de indicadores de control a partir de las metas del TP2." | Saqué una tolerancia que no estaba en mis metas y puse como responsables áreas de mi organigrama. |

Revisé todo lo que produjo la IA contra los apuntes de la cátedra. Cualquier error que quede es mío.
