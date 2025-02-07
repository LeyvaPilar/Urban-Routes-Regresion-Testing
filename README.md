# Urban-Routes-Regresion-Testing
Proyecto 1 

# Informe de Pruebas de Regresión - Urban Routes

## Introducción

El presente documento detalla los resultados de las pruebas de regresión realizadas sobre la aplicación Urban Routes, un sistema de navegación y mapeo urbano. El análisis se basa en la ejecución de 24 casos de prueba documentados en el archivo  que contiene dos hojas de trabajo principales: "Casos de prueba" e "Informes de errores".

<a href="https://docs.google.com/spreadsheets/d/1Tkh6WymfLPMW7f97s84083rNXOtFwH-H/edit?usp=sharing&ouid=103258639782325772763&rtpof=true&sd=true" target="_blank">
 📊​ Archivo original 
</a>

## Descripción del Proceso

Las pruebas fueron ejecutadas siguiendo un enfoque sistemático que abarcó:

1. **Validación de Funcionalidades Base**:
   - Navegación en el mapa (desplazamiento y zoom)
   - Sistema de búsqueda de direcciones
   - Interacción con elementos del mapa
   - Modos de visualización (satélite, relieve, pantalla completa)

2. **Metodología de Testing**:
   - Se ejecutaron pruebas de regresión para verificar la estabilidad de funcionalidades existentes
   - Cada caso de prueba fue documentado con:
     - Condiciones previas
     - Pasos de ejecución
     - Resultados esperados
     - Estado final de la prueba
   - Los errores encontrados fueron categorizados por severidad (Bloqueante, Medio, Bajo, Trivial)

3. **Documentación y Seguimiento**:
   - Se registraron 7 incidencias con su respectiva severidad y descripción detallada
   - Los casos fallidos fueron documentados con ID de error para seguimiento
   - Se incluyeron observaciones específicas para casos particulares

Las pruebas revelaron una combinación de problemas críticos y menores que afectan tanto la funcionalidad central como aspectos secundarios de la aplicación. Los resultados obtenidos proporcionan una base sólida para priorizar las correcciones necesarias y asegurar la calidad del producto.



# Resumen de Casos de Prueba - Urban Routes

## Datos Generales
| Categoría | Detalle |
|-----------|---------|
| Probador | Pilar Leyva Maldonado |
| Aplicación | Urban Routes |
| Total de Casos | 24 |

## Estado de los Casos
| Estado | Cantidad |
|--------|-----------|
| Aprobados | 13 |
| No Aprobados | 8 |
| Con Correcciones | 2 |
| Sin Estado | 1 |

## Detalle de Casos de Prueba

| ID | Título | Condición Previa | Resultado Esperado | Estado | ID Error |
|------|---------|------------------|-------------------|---------|-----------|
| CASO-1 | Desplazamiento del mapa | Abrir la aplicación Urban Routes | El mapa se mueve. Todos los objetos se muestran según el diseño. | Aprobado | - |
| CASO-2 | Zoom del mapa | La aplicación Urban Routes no debe estar abierta | El nivel de zoom aumenta en un valor. Todos los objetos se muestran según el diseño. | Aprobado | - |
| CASO-3 | No se puede hacer clic en los encabezados del área en el mapa | Abrir la aplicación Urban Routes | No ocurre nada. Los usuarios no pueden interactuar con los encabezados del mapa. | No aprobado | T003-1 |
| CASO-4 | No se puede hacer clic en los encabezados de la ciudad en el mapa | Abrir la aplicación Urban Routes | No ocurre nada. Los encabezados de la ciudad no se pueden seleccionar. | Aprobado | - |
| CASO-5 | Se puede seleccionar el campo "Desde" | Abrir la aplicación Urban Routes | Se selecciona el campo "Desde". El cursor parpadea. El campo de búsqueda está vacío. | No aprobado | T005-2 |
| CASO-6 | Se pueden buscar objetos en el campo "Hasta" | Abrir la aplicación Urban Routes | Se muestra la lista de estaciones de metro. | No aprobado | T006-3 |
| CASO-7 | El pin de la dirección aparece después de completar el campo "Desde" | Abrir la aplicación Urban Routes | El mapa hace zoom sobre el pin de la dirección seleccionada. | No aprobado | T007-4 |
| CASO-8 | El pin de la dirección aparece después de completar el campo "Hasta" | Abrir la aplicación Urban Routes | El mapa hace zoom sobre el pin de la dirección seleccionada. | No aprobado | T008-5 |
| CASO-9 | La dirección se elimina después de borrar el campo "Desde" | Abrir la aplicación Urban Routes. El campo "Desde" debe estar lleno | El campo se vacía. La dirección ingresada anteriormente se elimina del campo. | Aprobado | - |
| CASO-10 | La dirección se elimina después de borrar el campo "Hasta" | Abrir la aplicación Urban Routes. El campo "Hasta" debe estar lleno | El campo se vacía. La dirección ingresada anteriormente se elimina del campo. | Aprobado | - |

## Resumen de Errores Encontrados
| ID Error | Descripción |
|----------|-------------|
| T003-1 | Error en interacción con encabezados de área |
| T005-2 | Error en selección del campo "Desde" |
| T006-3 | Error en búsqueda del campo "Hasta" |
| T007-4 | Error en visualización del pin de dirección (Desde) |
| T008-5 | Error en visualización del pin de dirección (Hasta) |
| T0012-6 | Error en modo pantalla completa |
| T0024-7 | Error en visualización de información de la aplicación |




# Informe de Errores - Urban Routes

## Resumen de Severidades
| Severidad | Cantidad |
|-----------|----------|
| Bloquer | 3 |
| Medio | 1 |
| Bajo | 2 |
| Trivial | 1 |

## Detalle de Errores

| ID | Título | Severidad | Resultado Esperado | Resultado Actual |
|------|---------|------------|-------------------|-----------------|
| T003-1 | No se puede hacer clic en los encabezados del área en el mapa | Medio | Interacción del encabezado con los usuarios | El encabezado no genera ningún cambio al hacer clic sobre él |
| T005-2 | El campo de búsqueda "Desde" no se encuentra vacío | Bajo | Se selecciona el campo "Desde". El cursor parpadea. El campo de búsqueda está vacío | Al dar clic en el campo "Desde" el cursor parpadea, pero el campo no está vacío, aparece la siguiente leyenda: East 2nd Street, 601 |
| T006-3 | No se puede realizar ningún tipo búsqueda en "Hasta" | Bloquer | Encontrar opciones de búsqueda en "Hasta" | Al dar clic en "Hasta" para realizar alguna búsqueda o ingresar alguna dirección, permite ingresar los datos, pero no funciona el buscador |
| T007-4 | No se puede realizar ningún tipo de búsqueda en "Desde" | Bloquer | El mapa hace zoom sobre el pin de la dirección seleccionada | Al dar clic en "Desde" para realizar alguna búsqueda o ingresar alguna dirección, permite ingresar los datos, pero el buscador no genera ningún resultado |
| T008-5 | El pin de la dirección aparece después de completar el campo "Hasta" | Bloquer | El mapa hace zoom sobre el pin de la dirección seleccionada | Se ingresan los datos 1300 1st en "Hasta" no sucede nada, no aparece ningún pin y no genera ningún resultado en el mapa |
| T0012-6 | El modo de vista de pantalla completa se activa al hacer clic en el botón | Trivial | El modo de vista de pantalla completa no debe estar activado | El modo de pantalla completo está activado y, pese a que cumple el resultado esperado en las condiciones previas, se indica que no debe estar activo |
| T0024-7 | La información de la aplicación se muestra al hacer clic en el logotipo | Bajo | Se muestra la información sobre la aplicación | Al hacer clic en el logotipo de Urban Routes no sucede nada, no muestra información, el logotipo se queda totalmente estático |

## Distribución de Errores por Funcionalidad

| Funcionalidad | Cantidad de Errores |
|---------------|-------------------|
| Búsqueda y Navegación | 4 |
| Interfaz de Usuario | 2 |
| Interacción con Mapa | 1 |

