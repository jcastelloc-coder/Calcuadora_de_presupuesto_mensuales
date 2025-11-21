# Calculadora de Presupuesto Mensual

---

##  Introducción y Finalidad del Proyecto

La Calculadora de Presupuesto Mensual es una aplicación diseñada para ser una herramienta digital **práctica y eficiente** que permite a los usuarios llevar un control detallado de sus finanzas personales.

###  Finalidad y Propósito General

* **Finalidad:** Proporcionar un medio accesible para que el usuario pueda registrar sus ingresos y gastos, automatizando el cálculo del balance financiero mensual para obtener una visión clara y precisa de su estado económico.
* **Propósito:** Fomentar la **educación financiera personal**, reducir errores manuales en la gestión de cuentas y facilitar la toma de decisiones económicas más informadas.
* **A dónde quiere llegar (Evolución):** El proyecto evoluciona de una herramienta simple para cálculos en memoria (**Versión 1**) a un sistema robusto que incluye **almacenamiento local**, **gráficos**, **exportación de reportes en PDF** y **recomendaciones automáticas** (**Versión 2**), buscando convertirse en un recurso indispensable para la planificación económica personal.

### Alcance General
El sistema tiene un alcance inicialmente **local**, sin necesidad de conexión con servicios bancarios o la nube. Su objetivo es manejar y analizar datos de presupuesto directamente en el dispositivo del usuario.

---

##  Requerimientos Funcionales y No Funcionales – Versión 1

### Propósito y Alcance Específico
El sistema se centra en el registro simple y el cálculo inmediato del balance (Ingresos - Gastos). Su uso es local y su enfoque es la sencillez.

### Requerimientos Funcionales
| Descripción | Prioridad | Justificación |
| :--- | :--- | :--- |
| Permitir al usuario ingresar el monto total de ingresos mensuales. | Alta | Fundamental para el cálculo del balance. |
| Registrar y clasificar gastos mensuales por categorías. | Alta | Permite análisis detallado del presupuesto. |
| Calcular automáticamente el balance mensual (ingresos – gastos). | Alta | Núcleo funcional del sistema. |
| Mostrar un resumen con total de ingresos, total de gastos y balance resultante. | Media | Mejora comprensión y transparencia del resultado. |
| Permitir limpiar los datos ingresados para iniciar un nuevo cálculo. | Media | Facilita la usabilidad y continuidad de uso. |

### Requerimientos No Funcionales
| Descripción | Categoría | Prioridad |
| :--- | :--- | :--- |
| El sistema deberá tener una interfaz gráfica intuitiva y accesible. | Usabilidad | Alta |
| El tiempo de cálculo del balance no debe superar los 2 segundos. | Rendimiento | Alta |
| Los datos deberán mantenerse en memoria hasta que el usuario decida reiniciar o cerrar el sistema. | Fiabilidad | Media |

---

## Requerimientos Funcionales y No Funcionales – Versión Mejorada (V2)

### Propósito y Alcance Específico
El propósito es brindar una experiencia más robusta, incorporando persistencia de datos y análisis visuales.

### Requerimientos Funcionales
1.  Permitir ingresar ingresos y gastos de forma manual.
2.  Clasificación automática y manual por categorías.
3.  Generar gráficos de barras y pastel con el desglose mensual.
4.  Calcular balance mensual y anual.
5.  **Guardar datos localmente** para consulta futura.
6.  **Exportar reporte detallado en PDF**.
7.  **Ofrecer recomendaciones automáticas** según patrones detectados.
8.  Permitir editar, eliminar o actualizar registros previos.

### Requerimientos No Funcionales
* **Usabilidad:** Interfaz moderna, colores claros, navegación simple.
* **Seguridad:** Datos almacenados localmente con opción de bloqueo por clave.
* **Rendimiento:** Cálculos instantáneos, gráficos generados en menos de **2 segundos**.
* **Compatibilidad:** Disponible para PC y dispositivos móviles.
* **Fiabilidad:** Los datos permanecerán guardados aun si la app se cierra accidentalmente.

---

##  Plan de Pruebas

Las pruebas de software son el mecanismo esencial para garantizar que los requerimientos especificados se cumplan de forma precisa y verificable.

### Especificación de Pruebas (Simulado)
| Tipo de Prueba | Requerimiento Asociado | Datos de Entrada | Resultado Esperado | Resultado Obtenido (Simulado) |
| :--- | :--- | :--- | :--- | :--- |
| Prueba Unitaria 1 | RQ-01: El sistema debe permitir ingresar ingresos mensuales. | Ingreso = 52000 | El sistema almacena correctamente el valor 52000. | El ingreso se ha registrado exitosamente. |
| Prueba Unitaria 2 | RQ-02: El sistema debe permitir ingresar gastos mensuales. | Gasto = 1050 | El sistema almacena el valor 1050. | El gasto se registró exitosamente. |
| Prueba Unitaria 3 | RQ-03: El sistema debe calcular el balance mensual. | Ingreso total = 52000, Gasto total = 1050 | Balance = 50,950 | Balance mostrado: $50,950 |
| Prueba de Validación 1 | RQ-04: El sistema debe validar que los campos no estén vacíos. | Ingreso = “”, Gasto = 345 | Mostrar mensaje de error “Debe ingresar un valor válido”. | Mensaje mostrado correctamente. |
| Prueba de Validación 2 | RQ-05: El sistema debe aceptar solo valores numéricos. | Ingreso = “ABC”, Gasto = 135 | Mostrar error “Solo se permiten números”. | Error mostrado correctamente. |

---

##  Propuesta de Mantenimiento

### 1. Mantenimiento Correctivo
Se centra en resolver errores y fallos detectados durante el uso del sistema.

* **Acciones propuestas:** Corrección de errores en el registro, edición o eliminación de gastos; resolución de fallos en el cálculo de porcentajes; reparación de problemas visuales en gráficos.
* **Justificación:** Asegura que el sistema funcione correctamente.

### 2. Mantenimiento Adaptativo
Busca modificar el sistema para que se adapte a nuevas tecnologías, requisitos externos o cambios de entorno.

* **Acciones propuestas:** Ajustar la aplicación para nuevas resoluciones de dispositivos móviles; actualizar librerías o *frameworks* obsoletos; incorporar soporte para diferentes monedas o formatos de fecha.
* **Justificación:** Permite que el sistema continúe funcionando a medida que el entorno tecnológico evoluciona.

### 3. Mantenimiento Perfectivo
Consiste en mejoras para optimizar el rendimiento, usabilidad y funcionalidades.

* **Acciones propuestas:** Mejorar la velocidad del cálculo con grandes cantidades de datos; optimizar la carga del gráfico circular; rediseñar la interfaz para hacerla más intuitiva; agregar filtros avanzados.
* **Justificación:** Aumenta el valor del sistema, mejora la experiencia del usuario y extiende su ciclo de vida útil.

---

##  Reflexión sobre el Control de Versiones (Git)

El **Control de Versiones (VCS)** es la columna vertebral de la **confianza** y la **estabilidad** del proyecto, gestionando el crecimiento y asegurando la **precisión** del núcleo financiero.

### 1. Protegiendo la Lógica Financiera
* **Auditar la Precisión:** Cada *commit* documenta cambios en la lógica de cálculo. Esto es crucial para el **Mantenimiento Correctivo** (identificar cuándo se introdujo un error).
* **Aislamiento Crítico:** Se usa ramas para el desarrollo de ajustes menores, manteniendo el código matemático principal en la rama *main* seguro (**Rendimiento Alta**).

### 2. Planificando el Salto a la Persistencia de Datos
El **Mantenimiento Evolutivo** implica pasar de datos "en memoria" a almacenamiento local.

* **Desarrollo en Aislamiento Total:** Se utiliza una rama dedicada (`feature/almacenamiento-local`) para desarrollar la persistencia sin el riesgo de estropear la calculadora básica (**Fiabilidad**).
* **Gestión de Estructuras:** El VCS documenta la migración de estructuras de datos para asegurar la compatibilidad con versiones futuras.

### 3. Coordinación de la Usabilidad
* **Temas Paralelos:** El VCS permite trabajar simultáneamente en la mejora de estilos (Usabilidad) y la optimización de cálculos, fusionando ambos trabajos de manera segura (**Mantenimiento Perfectivo**).
