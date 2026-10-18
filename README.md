## 📌 Descripción del Proyecto

El objetivo de este proyecto es realizar la documentación y ejecución de pruebas (funcionales y de diseño) para el servicio de **compartir un automóvil** en la plataforma **Urban Routes**. 

Se aplicaron técnicas de diseño de pruebas como la **Partición de Clases de Equivalencia (ECP)** y el **Análisis de Valores Límite (BVA)** para validar tanto la interfaz visual como la lógica de la aplicación en dos entornos de prueba específicos.

---

## 🛠️ Entornos de Prueba

Las pruebas se ejecutaron bajo las siguientes configuraciones de navegador y resolución:

1. **Google Chrome** — Resolución: `800x600` (Pruebas de diseño y lógica)
2. **Mozilla Firefox** — Resolución: `1920x1080` (Pruebas de diseño)

---

## 📑 Estructura de la Documentación

La documentación del proyecto se divide en 5 secciones principales:

| Pestaña / Sección | Tipo de Documento | Descripción / Alcance |
| :--- | :--- | :--- |
| **1. Lista de comprobación del diseño** | Checklist | Validación de layout, ortografía, disposición de elementos, mapa de navegación y modales de confirmación/cancelación para la opción "Lujo". |
| **2. Lista de comprobación "Método de pago" y "Agregar tarjeta"** | Checklist (ECP / BVA) | Pruebas funcionales (positivas y negativas) para los campos de método de pago y vinculación de tarjeta bancaria. |
| **3. Casos de prueba para el botón "Reservar"** | Test Cases | Pruebas de habilitación/deshabilitación, estados visuales y textos dinámicos del botón "Reservar". |
| **4. Casos de prueba para la reserva** | Test Cases | Pruebas end-to-end de la lógica de reserva de automóvil, estados del viaje y temporizadores. |
| **5. Reportes de errores** | Bug Reports (Jira) | Documentación de errores detectados durante la ejecución de las pruebas. |

---

## 📋 Resumen de Casos de Prueba y Cobertura

### 1. Diseño del Formulario de Reserva (Tarifa "Lujo")
- [x] Verificación de ortografía y fuentes.
- [x] Layout y alineación del formulario en resoluciones `800x600` y `1920x1080`.
- [x] Mapa de navegación central e íconos de ruta.
- [x] Modales/Pop-ups:
  - *"Automóvil reservado"*
  - *"¿Seguro que quieres cancelar el viaje?"*
  - *"Viaje cancelado"*

### 2. Método de Pago y Agregar Tarjeta
- **Número de Tarjeta:** Validaciones de longitud (mínimo, máximo, caracteres numéricos y especiales).
- **Código CVV/CVC:** Validación de 3 dígitos, ocultamiento de caracteres y caracteres alfabéticos.
- **Botón Agregar:** Estado activo/inactivo según la validez de los campos.

### 3. Botón "Reservar"
- **Verificación de estado inactivo:** Cuando faltan campos obligatorios (licencia, tarjeta, etc.).
- **Verificación de estado activo:** Cuando todos los requisitos previos están cumplidos.
- **Texto dinámico:** Validación del formato de distancia y duración (`El recorrido será de [X] kilómetros y se hará en [Y] minutos`).

### 4. Flujo de Reserva de Automóvil
- Confirmación de la reserva y asignación del vehículo.
- Cancelación del viaje antes y durante la asignación.
- Comprobación del temporizador de espera.

---

## 🐞 Reporte de Defectos (Jira)

Los errores encontrados durante las ejecuciones fueron registrados en Jira siguiendo la estructura estándar de reporte de bugs:

* **Título / Resumen claro y conciso**
* **Entorno de prueba** (Navegador + Resolución)
* **Pasos para reproducir**
* **Resultado esperado vs. Resultado obtenido**
* **Prioridad y Severidad**
* **Captura de pantalla / Video de evidencia**
