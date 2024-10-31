# G14 - Documentación Proyecto LogiExpress Guatemala

## Integrantes

| Nombre                          | Carné      |
|---------------------------------|------------|
| Walter Manolo Martínez Mateo    | 201213212  |
| Luis Alfredo Vejo Mendoza       | 201212527  |
| Gabriel Orlando Ajsivinac Xicay | 201213010  |
| María Julissa García Morán      | 201602805  |
| Diego Abraham Robles Meza       | 201901429  |

## Introducción

LogiExpress Guatemala es un centro de distribución logístico que maneja productos perecederos, electrónicos y voluminosos. Este proyecto tiene como objetivo simular y optimizar las operaciones para reducir tiempos de espera, mejorar el uso de recursos y maximizar la eficiencia en el proceso de distribución.

## Diseño Explicado

El diseño del sistema actual incluye un flujo de operaciones que abarca desde la recepción de camiones hasta el despacho de pedidos. Cada proceso está representado por componentes específicos en el modelo, como se muestra en la figura:

- **Source1** y **Source5**: Representan las fuentes de entrada de productos (Electrónicos y Camiones).
- **Combiner2**: Combina los productos de las diferentes fuentes antes de pasar a la siguiente etapa.
- **Separator1**: Separa los productos clasificados hacia diferentes estaciones.
- **Sink3** y **Sink4**: Representan los puntos de salida final del proceso.

![Proyecto](Proyecto.png)

## Descripción de Procesos

1. **Recepción de Productos**: Los camiones llegan al centro logístico, descargan los productos y estos son dirigidos a la estación de clasificación.
2. **Clasificación de Productos**: Los productos se clasifican automáticamente en perecederos, electrónicos y voluminosos.
3. **Almacenamiento Temporal**: Los productos clasificados se almacenan en áreas específicas de acuerdo con su tipo.
4. **Empaque y Consolidación de Pedidos**: Los productos se consolidan en paquetes para satisfacer los pedidos de los clientes.
5. **Despacho de Pedidos**: Los paquetes consolidados son asignados a camiones para su entrega.

## Descripción de Variables de Estado

- **Cantidad de Productos en Espera**: Monitorea el número de productos que esperan ser clasificados.
- **Capacidad de Almacenamiento**: Controla el uso de espacio en cada área de almacenamiento.
- **Estado de Equipos**: Verifica la disponibilidad y funcionalidad de montacargas y otros equipos críticos.
- **Tiempo de Procesamiento**: Registra el tiempo total que cada producto pasa en el sistema.
- **Prioridad de Entrega**: Asigna la prioridad de cada pedido (estándar, rápido, urgente) para la organización de despachos.

## Descripción de Insights

Los siguientes insights son importantes para mejorar la eficiencia operativa del centro:

- **Tiempos de Espera**: Monitorear los tiempos de espera en la clasificación y en el almacenamiento para identificar cuellos de botella.
- **Utilización de Recursos**: Medir el uso de equipos (montacargas, vehículos AGV) para optimizar su disponibilidad y evitar tiempos muertos.
- **Capacidad de Almacenamiento**: Controlar el espacio utilizado en cada área para evitar saturaciones que afecten el flujo de productos.

## Conclusión

La simulación del centro de distribución LogiExpress Guatemala ha permitido una comprensión profunda de los puntos críticos en el flujo de operaciones logísticas. A través de la simulación, se han identificado áreas de oportunidad para optimizar el uso de recursos y reducir tiempos de espera, logrando así una mejora en la eficiencia general del sistema.

El control en tiempo real del estado de los equipos y la gestión de los recursos permiten responder de manera proactiva a eventos que, de no controlarse, podrían afectar la fluidez de las operaciones. Además, al ajustar el flujo de productos según la demanda y las prioridades de despacho, se pueden reducir considerablemente los cuellos de botella y minimizar los tiempos de espera en cada etapa del proceso.

El análisis también muestra que una adecuada priorización en el despacho de pedidos permite maximizar los ingresos, especialmente en pedidos urgentes que ofrecen mayores márgenes de ganancia. Sin embargo, esta estrategia requiere un equilibrio entre la disponibilidad de recursos y la priorización de entregas para evitar penalizaciones en caso de retrasos.

Finalmente, esta simulación establece una base sólida para implementar un modelo optimizado en el futuro, donde se integren ajustes en la asignación de operarios, mejoras en el mantenimiento preventivo de los equipos y una mejor organización de las zonas de almacenamiento. Estos cambios no solo incrementarían la eficiencia operativa, sino que también contribuirían a la satisfacción del cliente mediante un servicio más rápido y confiable. La implementación de un modelo visualmente atractivo en 3D también permitirá a los stakeholders comprender mejor el sistema, facilitando la toma de decisiones estratégicas en el manejo del centro de distribución.


