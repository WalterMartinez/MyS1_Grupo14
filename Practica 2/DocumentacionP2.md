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

* **Proceso "Cantidad Orden"<br>**
El proceso se inicia con una decisión (Decide) y va avanzando por diferentes etapas en donde se van asignando la cantidad de flores, el proceso evalúa dichas flores una por una para ir asignando las cantidades correspondientes, una vez se cumpla la cantidad requerida el pedido está listo. En el componente *Assign* se configuró el valor de la probabilidad que tiene cada producto en venir dentro de un pedido.

* **Proceso "Enviar Orden"<br>**
Este proceso se encarga de crear los arreglos florales según las ordenes recibidas. Cada *Create* se encarga de crear las cantidades de flores recibidas en las ordenes para ir creando los arreglos y luego se transfiere al paso siguiente.

* **Proceso "Pedir Caja"**<br>
Este proceso gestiona el empaque de los pedidos, asegurando que los arreglos florales sean empacados de manera eficiente y agrupados para el transporte posterior. Se hace uso de *Design* para realizar asignaciones iniciales relacionadas con la caja que se va a usar, luego se hace el uso de *Decide* en varios puntos del proceso encargados de verificar que las condiciones son correctas para continuar, también se usa *UnBatch* para desagrupar los pedidos y ser tratado de manera individual, luego con un *Batch* para volver a empaquetar los pedidos y ser enviados.

* **Proceso "ParentInput_Transporte_Entered"**<br>
Este proceso se encarga de enviar una nueva caja cuando la caja actual ha llegado a su capacidad máxima de productos dentro de ella.

* **Proceso "Pedir Producto"**<br>
Este proceso se encarga de realizar la espera de 15 segundos entre el momento que el pedido es realizado y cuando el sistema lo empieza a procesar.

### Descripción de los estados utilizados

Los estados en los que se basa el sistema son los siguientes:

* **Recepción de orden:** El sistema recibe una solicitud con los parámetros del cliente.
* **Selección de flores:** Según las preferencias, se elige el tipo de flor a incluir en el ramo.
* **Determinación de cantidades:** Se calcula la cantidad de cada flor, dependiendo del tamaño del ramo solicitado.
* **Envío al sistema automatizado:** Las flores seleccionadas son preparadas para ser enviadas al área de empaquetado y distribución.
* **Empaquetado:** El ramo es preparado y empaquetado de manera automatizada para su envío.
* **Estado de envío:** El ramo final es enviado al cliente y el sistema actualiza el estado como completado.

### Conclusión

La implementación de este sistema permite una automatización eficiente del proceso de creación de ramos de flores, reduciendo el tiempo de respuesta y optimizando el uso de recursos. La elección de flores basada en probabilidades asegura una personalización acorde a las preferencias del cliente, lo que mejora la experiencia del usuario.

### Propuesta de mejora
Nuestro modelo trabaja de manera eficiente, ya que ningún servidor llega al 50% de uso. Por lo que para reducir costos y hacer más eficiente el proceso se está considerando unificar la revisión de flor con la revisión de peso en una máquina, garantizando una revisión sin demoras innecesarias.