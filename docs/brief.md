# Brief de Proyecto: QuickMap
**Versión de Documento:** 1.0  
**Fecha:** 23 de Agosto de 2026  
**Materia:** Gestión Aplicada al Desarrollo de Software II (3665)  
**Universidad Nacional de La Matanza (UNLaM)**

---

### 1. Integrantes del Equipo
* **Nombre del Equipo:** QuickMap
* **Repositorio GitHub:** `gadsii-quickmap`
* **Miembros:**
  * Facundo Carballo
  * Matias Garcia Burgio
  * Federico Castro
  * Agostina Mottura
  * Ignacio Romero

#### Descripción:

QuickMap es una herramienta destinada a los estudiantes de la UNLaM que permite visualizar de forma clara y actualizada su progreso académico. A través de un mapa interactivo de la carrera, muestra las materias aprobadas, las correlatividades disponibles, el camino crítico, el promedio y el porcentaje de avance, facilitando la planificación de las próximas materias a cursar y adaptándose a los cambios en los planes de estudio.

---

### 2. Segmento Elegido y Acceso a los Usuarios

#### El Segmento
El segmento seleccionado de la comunidad UNLaM está conformado por los **estudiantes de los primeros años (1° y 2° año) de las carreras de la UNLaM**.

* **Descripción y Tamaño Estimado:** La UNLaM cuenta con una matrícula activa superior a los 60.000 estudiantes. Se estima que el grupo de ingresantes y alumnos de primeros años representa entre un 25% y un 30% del total (aproximadamente entre 15.000 y 18.000 alumnos). Estos alumnos transitan los ciclos básicos, introductorios o las primeras materias específicas de sus respectivas carreras.
* **Qué los distingue del resto:** Provienen principalmente de la escuela secundaria, un entorno con una estructura curricular rígida donde las materias y los horarios están preestablecidos de manera automática. Al ingresar a la universidad, se enfrentan por primera vez a un modelo de autogestión: deben decidir cuántas y cuáles materias cursar en cada cuatrimestre, interpretar regímenes de correlatividades complejos y entender cómo impactan sus notas en su avance académico. Al estar en su etapa inicial, no disponen de una red de contactos consolidada (compañeros de años avanzados, graduados o docentes) que los oriente en la toma de decisiones estratégicas de cursada.
* **Por qué este segmento y no otro:** Los estudiantes de primeros años son los que experimentan el mayor nivel de desorientación inicial y frustración curricular. Son los más propensos a cometer errores de inscripción (como cursar materias secundarias y postergar materias "clave"), lo que genera demoras involuntarias en sus carreras y, en el peor de los casos, deserción temprana. Al enfocar el producto en este segmento, QuickMap ataca el problema de raíz en su punto más crítico. Además, es un segmento altamente escalable: un ingresante que adopte QuickMap lo seguirá utilizando como usuario a lo largo de toda su carrera universitaria.

#### El Acceso a los Usuarios
Para validar nuestras hipótesis y probar la solución, hemos seleccionado a tres usuarios reales que pertenecen estrictamente a nuestro segmento y que representan a diferentes departamentos de la UNLaM para asegurar diversidad de perspectivas académicas:

1. **Usuario 1 (U1): Agustín Larizza**
   * **Rol:** Estudiante de 1° año de la Tecnicatura en Desarrollo Web (Departamento de Ingeniería e Investigaciones Tecnológicas - DIIT).
   * **Origen/Relación:** Amigo cercano de un integrante del equipo. Llegamos a él de manera directa en el ámbito social.
   * **Disponibilidad:** Confirmada explícitamente para las dos instancias de validación: el relevamiento de necesidades (TP2 - última semana de agosto) y la prueba de usabilidad del MVP (TP5 - última semana de septiembre).

2. **Usuario 2 (U2): Gonzalo Carballo**
   * **Rol:** Estudiante de 2° año de la Licenciatura en Nutrición (Departamento de Ciencias de la Salud).
   * **Origen/Relación:** Hermano de uno de los integrantes de nuestro equipo. Declaramos esta relación con total transparencia, reconociendo que sus respuestas pueden estar influenciadas por el deseo de apoyar nuestro proyecto. Mitigaremos este sesgo contrastando minuciosamente sus opiniones con el resto de los participantes independientes.
   * **Disponibilidad:** Confirmada explícitamente para las dos instancias de validación: el relevamiento de necesidades (TP2 - última semana de agosto) y la prueba de usabilidad del MVP (TP5 - última semana de septiembre).

3. **Usuario 3 (U3): Martina Bartoli**
   * **Rol:** Estudiante de 1° año de la carrera de Medicina (Departamento de Ciencias de la Salud).
   * **Origen/Relación:** Amiga cercana de un integrante de nuestro equipo. Llegamos a ella de manera directa mediante actividades de ocio compartidas.
   * **Disponibilidad:** Confirmada explícitamente para las dos instancias de validación: el relevamiento de necesidades (TP2 - última semana de agosto) y la prueba de usabilidad del MVP (TP5 - última semana de septiembre).

---

### 3. Definición del Producto

* **Nombre del Producto:** QuickMap
* **Problema concreto que resuelve y a quién:** Resuelve la falta de visibilidad del avance académico y la desorientación en la planificación curricular que sufren los estudiantes de los primeros años de la UNLaM. Les evita tomar decisiones ineficientes de inscripción y demorarse en la carrera al no comprender las relaciones de correlatividad ocultas en planes de estudio en formato texto o PDF.

#### Funcionalidades CORE
1. **Mapa de Correlatividades Interactivo (Visualizador de Red):** En lugar de un listado textual, QuickMap ofrece un mapa visual e interactivo del plan de estudios de la carrera del usuario, donde las materias se representan como nodos interconectados. Al seleccionar una materia, se destacan claramente sus correlativas necesarias (hacia atrás) y las asignaturas que habilita (hacia adelante).
2. **Seguimiento Dinámico del Progreso Académico:** Clasificación visual automática de las materias según su estado académico actual mediante una gama de colores intuitiva: *Aprobada* (con nota final), *Cursando* (en cuatrimestre activo), *Regular* (cursada aprobada, final pendiente), *Habilitada para cursar* (cumple con las correlativas) y *Bloqueada* (faltan correlativas).
3. **Proyección del Camino Crítico:** Un motor de sugerencia que resalta la ruta óptima de asignaturas prioritarias que el estudiante debería cursar en el siguiente cuatrimestre para maximizar su avance y evitar bloqueos a futuro por materias con alta densidad de correlatividades.
4. **Simulador de Promedio e Inscripción:** Un módulo que permite al estudiante realizar simulaciones de calificaciones en materias cursando o proyectar cuatrimestres futuros. El sistema calcula en tiempo real el promedio proyectado (con y sin aplazos), el porcentaje de progreso general de la carrera y desbloquea dinámicamente las materias resultantes en el mapa.

#### Integraciones Tecnológicas Previstas
* **Sistema de Autenticación de Usuarios de la UNLaM (OAuth / Intraconsulta):** Necesario para verificar de forma segura que el usuario es un alumno regular de la UNLaM y asegurar que solo él pueda ver y operar sobre sus datos de rendimiento académico, resguardando la privacidad de la información.
* **API de Notas e Historial Académico de la UNLaM (o scraper simulado de Intraconsulta):** Es indispensable para extraer automáticamente el historial académico real del alumno (materias aprobadas, notas, planes de estudio activos). Esto evita que el estudiante tenga que cargar manualmente su historial (proceso propenso a errores y abandono) y asegura que el mapa de correlativas, el progreso y el promedio acumulado se sincronicen en tiempo real de manera transparente ni bien se carga un acta de examen en Intraconsulta.

---

### 4. Identificar los Grupos de Usuarios

El producto interactuará con dos perfiles de usuarios diferenciados dentro de la comunidad de estudiantes de la UNLaM:

#### Grupo 1: Estudiantes de primeros años (Grupo Primario)
* **Quiénes son:** Estudiantes que están cursando su primer o segundo año de carrera en la UNLaM, usualmente recién salidos del secundario.
* **Relación con el problema:** Tienen muy poco conocimiento sobre cómo gestionar su carrera, no comprenden del todo las correlativas y se sienten abrumados por la transición de tener un horario escolar preestablecido a tener que planificar autónomamente su cursada.
* **Qué los motivaría a usar QuickMap:** Encontrar una herramienta amigable, visual y libre de burocracia que les diga exactamente qué materias pueden cursar, cuáles les conviene priorizar para avanzar más rápido y cómo organizar sus próximos cuatrimestres sin cometer errores que retrasen su graduación.

#### Grupo 2: Estudiantes intermedios o avanzados (Grupo Secundario)
* **Quiénes son:** Estudiantes en su tercer año o superior, que ya dominan los procesos administrativos de la universidad.
* **Relación con el problema:** Aunque entienden el sistema, invierten tiempo excesivo en Excel o anotadores manuales para proyectar promedios, simular escenarios en base a su carga laboral, u organizar las materias restantes cuando ocurren cambios de plan de estudios.
* **Qué los motivaría a usar QuickMap:** Ahorrar tiempo administrativo mediante la automatización de sus proyecciones de promedio, utilizar el simulador interactivo para planificar su egreso y evaluar rápidamente las alternativas de inscripción ante horarios laborales restrictivos.

#### Justificación del Grupo Primario
Hemos seleccionado a los **Estudiantes de Primeros Años** como nuestro grupo primario de análisis y diseño. Un estudiante avanzado ya ha desarrollado estrategias (manuales y costosas en tiempo) para sobrevivir al sistema. En cambio, en los primeros años es donde se genera el mayor dolor inicial, donde se toman decisiones erróneas por falta de información y donde una solución como QuickMap tiene el mayor poder preventivo, evitando la deserción y optimizando el trayecto educativo desde el día uno.

---

### 5. Los Supuestos del Proyecto

Hemos identificado los siguientes supuestos que consideramos verdaderos para el diseño de nuestro producto, los cuales validaremos empíricamente con nuestros usuarios primarios a lo largo del cuatrimestre:

* **Supuesto 1:** *"Asumimos que los estudiantes de los primeros años de la UNLaM experimentan confusión y cometen errores al planificar sus cuatrimestres debido a la dificultad para interpretar el formato de planes de estudio tradicionales (texto plano o PDFs) provistos por la facultad."*
* **Supuesto 2 (SUPUESTO CRÍTICO):** *"Asumimos que el desconocimiento del 'camino crítico' de correlativas óptimas de una carrera genera que los estudiantes de los primeros años tomen decisiones de inscripción ineficientes, provocando retrasos no deseados en sus fechas de egreso."*
* **Supuesto 3:** *"Asumimos que los estudiantes están dispuestos a iniciar sesión con sus credenciales universitarias (o un token de integración) dentro de QuickMap con tal de obtener su historial de materias sincronizado de forma automática en tiempo real."*
* **Supuesto 4:** *"Asumimos que los estudiantes realizan actualmente un seguimiento paralelo e informal de sus promedios y avance curricular mediante herramientas analógicas o digitales externas (ej. planillas de Excel, anotaciones en cuadernos, grupos de WhatsApp)."*
* **Supuesto 5:** *"Asumimos que los estudiantes se sienten frustrados y desorientados al enfrentar un cambio de plan de estudios en su carrera (como ha sucedido en informática o medicina), por no comprender la tabla de equivalencias de materias."*
* **Supuesto 6:** *"Asumimos que la UNLaM no planea desarrollar ni integrar una interfaz visual interactiva de planes de estudios y correlativas dentro de Intraconsulta en el corto o mediano plazo."*
* **Supuesto 7:** *"Asumimos que una visualización clara del porcentaje exacto de avance de la carrera y el promedio dinámico actúa como un factor motivacional positivo que incentiva al alumno a continuar con sus estudios en momentos de frustración académica."*
