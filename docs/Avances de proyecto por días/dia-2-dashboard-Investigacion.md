## Qué es un Dashboard
  > Una pantalla que se actualiza sola y te dice “todo sigue normal” o “aquí algo se está saliendo de lo común”.
  > Un dashboard es un tablero de alertas visuales para no tener que buscar a ciegas todo el día.
  


## Funciones concretas:

     1 Visibilidad inmediata
       El SOC ve en segundos si algo se está desviando de lo normal: picos de errores, logins fallidos, tráfico raro, hosts ruidosos.

     2 Priorización
      No todo es incidente. El dashboard permite ver qué merece atención ahora y qué puede esperar.

     3 Monitoreo continuo
      Mientras el analista hace otra cosa, el dashboard sigue ejecutando búsquedas y “vigila” el entorno.

     4 Reducción de ruido
      Resume miles o millones de eventos en indicadores simples (contadores, tendencias, top N).

     5 Detección temprana
      Muchos ataques se ven primero como patrones, no como alertas claras. El dashboard muestra esos patrones.

     6 Cambio de turno
      El analista entrante ve el estado del ambiente sin leer reportes largos.

## Crear un dashboard en Splunk (paso a paso, básico)

 >Objetivo: pasar de una búsqueda a un panel visible que se actualiza solo.

  1. Ir a Search & Reporting
   Este es el único lugar donde se crean búsquedas reales.

  2. Hacer una búsqueda simple
   Ejemplo genérico:

   index=_internal | head 20


   No importa el contenido todavía. La idea es ver resultados.

  3. Ajustar el rango de tiempo
   Arriba a la derecha:

   Últimos 15 minutos o 24 horas
   El dashboard siempre depende del tiempo seleccionado.

  4. Convertir la búsqueda en panel
   Arriba a la derecha:

   Click en Save As

   Elegir Dashboard

  5. Crear dashboard

   Nombre: algo claro (ej. SOC - Pruebas Autenticación)

   Descripción: qué muestra

   Tipo: Classic Dashboard (más simple para aprender)

   Permisos: Private (por ahora)

  6. Elegir visualización
   Splunk te pide cómo mostrarlo:

   Tabla (recomendado al inicio)

   Barra

   Línea


  7. Guardar

Los dashboards en Splunk son paneles que muestran resultados de búsquedas guardadas de forma visual y fácil de entender. Se usan para ver rápidamente qué está pasando en los sistemas, sin necesidad de revisar logs uno por uno. Cada panel representa una búsqueda y se actualiza según el tiempo seleccionado.

En un entorno SOC, los dashboards sirven para monitorear, no para investigar en detalle. Ayudan a detectar cosas fuera de lo normal, como muchos errores, intentos fallidos de acceso o comportamientos repetitivos. Cuando algo llama la atención, el analista abre la búsqueda que alimenta ese panel y continúa el análisis en Search & Reporting.