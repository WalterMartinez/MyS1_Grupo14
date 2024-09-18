## Documentación Práctica 2 MyS1 - _Grupo No. 14_

### Integrantes:

| Nombre                          |   Carné   |
| :------------------------------ | :-------: |
| Walter Manolo Martinez Mateo    | 201213212 |
| Luis Alfredo Vejo Mendoza       | 201212527 |
| Gabriel Orlando Ajsivinac Xicay | 201213010 |
| María Julissa García Morán      | 201602805 |
| Diego Abraham Robles Meza       | 201901429 |

### Diseño del sistema

El sistema está conformado por un servidor encargado de gestionar las órdenes recibidas. El flujo de trabajo sigue una secuencia predefinida que abarca las siguientes etapas: selección de flores, preparación del ramo y envío a la sección del Sistema Automatizado. Las flores disponibles para la selección incluyen Rosas, Orquídeas, Lirios, Tulipanes y Girasoles. Cada tipo de flor tiene una probabilidad de selección determinada según preferencias del cliente, lo que optimiza el proceso de elaboración del ramo.

### Descripción de procesos utilizados

Se implementaron procesos independientes para la selección de cada tipo de flor. Se asignó una probabilidad de selección a cada tipo de flor: Rosas, Orquídeas, Lirios, Tulipanes y Girasoles. Una vez realizada la selección, se define la cantidad de cada flor que será agregada al ramo. Finalmente, el ramo es procesado por el Sistema Automatizado, que se encarga del empaquetado y envío final.

### Descripción de los estados utilizados

Los estados en los que se basa el sistema son los siguientes:

Recepción de orden: El sistema recibe una solicitud con los parámetros del cliente.
Selección de flores: Según las preferencias, se elige el tipo de flor a incluir en el ramo.
Determinación de cantidades: Se calcula la cantidad de cada flor, dependiendo del tamaño del ramo solicitado.
Envío al sistema automatizado: Las flores seleccionadas son preparadas para ser enviadas al área de empaquetado y distribución.
Empaquetado: El ramo es preparado y empaquetado de manera automatizada para su envío.
Estado de envío: El ramo final es enviado al cliente y el sistema actualiza el estado como completado.

### Conclusión

La implementación de este sistema permite una automatización eficiente del proceso de creación de ramos de flores, reduciendo el tiempo de respuesta y optimizando el uso de recursos. La elección de flores basada en probabilidades asegura una personalización acorde a las preferencias del cliente, lo que mejora la experiencia del usuario.
