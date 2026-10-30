# Mecanismos de control: indicadores y estándares de desempeño

El control cierra el proceso administrativo que empezó con la planificación de la Entrega 2. Consiste en comparar el resultado real contra un estándar fijado de antemano, aplicar una acción correctiva si aparece un desvío y retroalimentar la planificación. Los estándares salen de las metas del TP2 y de la métrica guardrail definida en el TP3, los datos para medirlos del diccionario de datos del TP3, y los responsables son áreas del organigrama del TP3.

| Indicador | Cómo se mide | Estándar | Frecuencia | Responsable | Acción si no se cumple |
| --- | --- | --- | --- | --- | --- |
| Tasa de conversión por variante | Visitas con convirtio verdadero sobre el total de visitas de cada variante (PostHog) | La variante test convierte al menos un 8% más que control (línea base) | Semanal; se mide durante las primeras 4 semanas y se decide cuando se alcanza la muestra | Product Management y Marketing | Se descarta el diseño nuevo o se itera una nueva versión |
| Tamaño de muestra | Cantidad de solicitudes enviadas por variante | Mínimo 2.000 solicitudes por variante y confianza ≥95% | Semanal | Product Management | Se extiende la medición y no se toma ninguna decisión hasta alcanzarlo |
| Tasa de aprobación (guardrail) | Solicitudes aprobadas sobre solicitudes con resultado (aprobadas más rechazadas), por variante (campo estado de Solicitud) | La tasa de test no es menor que la de control | Semanal | Product Management y Marketing | Se pausa el experimento, se avisa a la Gerencia de Riesgo Crediticio y se revisa el formulario |
| Latencia del feature flag | Tiempo que el SDK de PostHog agrega a la carga de la página | No más de 200 ms | Continua (monitoreo) | Ingeniería de Software | Se pausa el experimento (todos ven la versión actual) y se revisa la integración del SDK |
| Capacidad | Solicitudes concurrentes que la página soporta sin degradación | 5.000 concurrentes | Antes del lanzamiento (prueba de carga) | Equipo DevOps y Equipo QA | Se ajusta la infraestructura antes de lanzar |
| Cumplimiento del plazo | Avance real comparado con el diagrama de Gantt | 11 semanas | Semanal | Product Management | Se replanifican tareas y responsables |

La latencia tiene una alerta automática que se publica en un canal compartido apenas se supera el estándar. El equipo de Ingeniería de Software analiza el desvío: si es un problema del sistema lo corrige, y si no, lo comunica a Product Management. Los indicadores con frecuencia semanal los revisa su responsable, que compara el valor real con el estándar y, si hay un desvío, lo comunica a Product Management para decidir la acción correctiva.

Los dos primeros indicadores miden si el experimento cumple su objetivo. El tercero es una métrica de resguardo: evita que un diseño atraiga más solicitudes que después se rechazan. Los tres últimos controlan que el sistema funcione y que el proyecto avance según lo planificado.

Para la auditoría técnica, cada indicador se puede verificar con datos del propio sistema: los tres primeros salen de las entidades Visita y Solicitud del diccionario de datos, la latencia y la capacidad de las herramientas de monitoreo, y el plazo del tablero de GitHub Projects y del Gantt.
