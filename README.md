# dIArio — Tu diario personal con inteligencia artificial

**De los datos cotidianos a los descubrimientos personales.**

dIArio es un diario personal inteligente diseñado para transformar la información dispersa de la actividad digital en una visión coherente, personalizada y útil de la vida cotidiana.

Mediante la conexión con calendarios, correos electrónicos, aplicaciones de mensajería, servicios de localización, actividad física y reflexiones personales, dIArio pretende reconstruir las experiencias diarias, identificar compromisos pendientes, descubrir patrones personales y generar recomendaciones que ayuden a tomar decisiones más conscientes.

Más allá de resumir información, el proyecto explora cómo combinar agentes de inteligencia artificial, memoria a largo plazo, modelos multimodales e ingeniería cloud-native para construir un asistente personal de IA fiable y útil.

El objetivo no es simplemente desarrollar una aplicación que utilice inteligencia artificial, sino diseñar, desarrollar, evaluar y desplegar una solución integral siguiendo prácticas profesionales de ingeniería de software e inteligencia artificial.

**Proyecto:** Trabajo Final de Máster — Inteligencia Artificial, Cloud Computing y DevOps, Pontia.

**Estado:** Propuesta de proyecto y exploración de arquitectura.

---

## 1. Visión y objetivos

Nuestra vida digital está distribuida entre múltiples aplicaciones. Los calendarios contienen compromisos, los correos y mensajes recogen decisiones, las aplicaciones deportivas registran actividad física y los mapas proporcionan contexto sobre nuestras rutinas diarias.

Sin embargo, esta información rara vez ofrece una visión unificada de cómo empleamos nuestro tiempo, qué es importante para nosotros o qué hábitos se relacionan con nuestro bienestar personal.

dIArio pretende cubrir esta necesidad combinando información de diferentes fuentes para construir un diario personal estructurado, consultable y evolutivo.

### Objetivos principales

- **Comprender el día:** reconstruir los acontecimientos relevantes y generar resúmenes diarios coherentes y personalizados.
- **Gestionar compromisos:** identificar posibles tareas, fechas límite y próximos eventos.
- **Construir memoria personal:** conservar el contexto histórico relevante y recuperarlo cuando sea necesario.
- **Descubrir patrones:** explorar relaciones entre actividades, rutinas, objetivos personales y bienestar declarado por el usuario.
- **Proponer recomendaciones:** sugerir mejoras realistas relacionadas con la actividad física, las relaciones sociales, la productividad, el ocio y las finanzas personales.
- **Crear una experiencia multimodal:** transformar los resúmenes diarios en episodios de audio narrados, similares a un podcast personal.
- **Desarrollar una solución integral:** combinar ingeniería de software, IA, infraestructura cloud, automatización, seguridad y observabilidad.

El principio fundamental es ayudar a las personas a comprender mejor su vida y tomar sus propias decisiones, sin delegar en un algoritmo la definición de aquello que debería hacerlas felices.

## 2. Funcionalidades principales

### 2.1. Recopilación unificada de información personal

dIArio integrará información procedente de diferentes aplicaciones mediante conectores independientes.

Entre las fuentes potenciales se encuentran:

- Calendarios y herramientas de gestión de tareas.
- Correo electrónico personal y profesional.
- Aplicaciones de mensajería.
- Mapas, localización y movilidad.
- Aplicaciones de actividad física y salud.
- Finanzas personales y registros de gastos.
- Entradas manuales del diario y objetivos definidos por el usuario.

El sistema normalizará la información de estas fuentes en una representación común, conservando las marcas temporales, la procedencia y los metadatos relevantes.

El prototipo inicial podrá utilizar API simuladas y conjuntos de datos sintéticos, lo que permitirá demostrar el flujo completo sin depender del acceso a cuentas privadas ni de los permisos de plataformas externas.

### 2.2. Diario diario automatizado

La aplicación combinará acontecimientos relevantes para construir una cronología del día y generar un resumen en lenguaje natural.

El proceso incluirá validación de datos, eliminación de duplicados, clasificación de eventos, síntesis contextual y persistencia de resultados.

Las entradas generadas distinguirán entre información observada, inferencias producidas por el modelo y reflexiones personales. El usuario podrá revisar y editar el diario resultante.

### 2.3. Gestión inteligente de tareas y compromisos

dIArio identificará posibles compromisos a partir de correos, mensajes, calendarios y otras fuentes autorizadas.

Ayudará a detectar tareas pendientes, fechas límite próximas y acciones que podrían haberse olvidado.

Las tareas inferidas se distinguirán de los compromisos confirmados, permitiendo al usuario aprobarlas, modificarlas o descartarlas antes de convertirlas en acciones efectivas.

### 2.4. Memoria a largo plazo e insights personales

El sistema mantendrá una visión histórica de acontecimientos relevantes, entradas del diario, preferencias y objetivos definidos por el usuario.

Combinando análisis estructurado de datos, recuperación semántica e IA generativa, dIArio explorará preguntas como:

- ¿Qué actividades suelen coincidir con los días que valoro más positivamente?
- ¿Cómo evolucionan mis rutinas a lo largo del tiempo?
- ¿Dedico suficiente tiempo al ejercicio, al ocio y a las relaciones sociales?
- ¿Qué hábitos podrían ayudarme a organizar mejor mi tiempo?
- ¿Dónde podría identificar oportunidades de ahorro?
- ¿Qué actividades podrían ayudarme a introducir variedad en mi rutina?

Las recomendaciones estarán fundamentadas en la evidencia disponible y se presentarán como hipótesis o sugerencias, no como relaciones causales demostradas ni como diagnósticos psicológicos.

### 2.5. Podcast diario personalizado

dIArio ofrecerá la posibilidad de escuchar una versión narrada del día.

Un modelo de lenguaje generará un guion basado en el diario, que posteriormente se convertirá en audio mediante un servicio de síntesis de voz.

El proceso de generación se diseñará como un flujo asíncrono, de modo que el usuario pueda consultar el diario mientras se prepara el podcast.

### 2.6. Interacción con supervisión humana

El usuario conservará el control sobre su información personal y las acciones relevantes.

Podrá corregir acontecimientos, editar resúmenes, confirmar tareas, valorar recomendaciones e inspeccionar la información que sustenta los insights generados.

Las acciones externas sensibles requerirán autorización explícita.

---

## 3. Arquitectura de IA y orquestación inteligente

dIArio explorará una arquitectura modular de inteligencia artificial que combine componentes de software deterministas con agentes especializados.

Entre las posibles responsabilidades se encuentran la interpretación de datos, la extracción de eventos, la identificación de tareas, la síntesis diaria, la recuperación de recuerdos, el análisis de patrones y la generación de audio.

Una capa de orquestación coordinará los componentes necesarios, validará los resultados intermedios y gestionará los errores.

El proyecto estudiará **Model Context Protocol (MCP)** como mecanismo estandarizado para exponer herramientas y fuentes de información a los componentes de IA. Las integraciones simuladas permitirán demostrar esta arquitectura antes de incorporar conexiones reales seleccionadas.

El diseño priorizará flujos controlados y verificables frente a una autonomía innecesaria de los agentes. No todas las operaciones necesitan un modelo de lenguaje: la normalización de datos, la eliminación de duplicados, los cálculos y las validaciones deben resolverse mediante software convencional siempre que sea apropiado.

La capa de memoria combinará persistencia estructurada con recuperación semántica, permitiendo recuperar información histórica relevante sin enviar todo el historial del usuario al modelo en cada petición.

La selección de modelos, las estrategias de orquestación y los frameworks de integración se evaluarán según su utilidad, complejidad, fiabilidad y coste.

## 4. Cloud Computing y DevOps

dIArio se diseñará como una aplicación integral que pueda ejecutarse localmente y desplegarse en un entorno cloud.

El proyecto explorará las siguientes áreas:

- **Desarrollo del backend:** desarrollo modular en Python, programación orientada a objetos, creación de API y validación de datos.
- **Contenedorización:** entornos reproducibles mediante Docker.
- **Entrega automatizada:** control de versiones, revisión de código, pruebas automatizadas y pipelines CI/CD con GitHub Actions.
- **Despliegue cloud:** ejecución de servicios, almacenamiento persistente, configuración segura y acceso a servicios de IA.
- **Infraestructura como código:** aprovisionamiento reproducible de infraestructura cuando resulte apropiado.
- **Procesamiento asíncrono:** ejecución en segundo plano de sincronizaciones, análisis y generación de audio.
- **Observabilidad:** registros estructurados, trazas de ejecución, métricas de rendimiento y monitorización de errores.
- **Resiliencia:** reintentos controlados, límites de tiempo, prevención de duplicados y recuperación de flujos fallidos.

AWS y Azure se considerarán como posibles plataformas de despliegue. La arquitectura cloud definitiva y la selección de servicios se acordarán durante la fase de diseño del proyecto.

El objetivo es demostrar un proceso de despliegue reproducible y una separación clara entre el código de la aplicación, la configuración y la infraestructura.

## 5. Calidad, evaluación y observabilidad de la IA

Uno de los elementos diferenciadores de dIArio será la evaluación del comportamiento de la IA, en lugar de depender exclusivamente de demostraciones subjetivas.

Se utilizará un conjunto representativo de escenarios diarios sintéticos para evaluar la calidad de los resultados generados y la fiabilidad del flujo de trabajo completo.

La estrategia de evaluación tendrá en cuenta:

- Precisión y completitud de los eventos y tareas extraídos.
- Consistencia factual de los resúmenes diarios.
- Relevancia de los recuerdos históricos recuperados.
- Evidencia que respalda las recomendaciones.
- Fiabilidad de las llamadas a herramientas y los flujos de agentes.
- Latencia, consumo de tokens y coste estimado.
- Comportamiento ante entradas incompletas, ambiguas o adversariales.

Cuando sea posible, la evaluación combinará comprobaciones deterministas, ejemplos etiquetados y revisión humana. Los evaluadores basados en modelos podrán complementar estos métodos, pero no se considerarán una fuente de verdad infalible.

La observabilidad permitirá conocer qué componentes se han ejecutado, dónde se han producido errores, cuánto han tardado las operaciones y cuánto cuesta cada flujo, minimizando al mismo tiempo la exposición de información personal en la telemetría.

El proyecto buscará establecer criterios de calidad medibles y pruebas de regresión para evaluar sistemáticamente los cambios en modelos, prompts u orquestación.

## 6. Seguridad, privacidad e IA responsable

Dado que dIArio podría procesar comunicaciones personales, información de localización, registros de actividad y datos financieros, la seguridad y la privacidad serán aspectos centrales del diseño.

El proyecto tendrá en cuenta:

- Consentimiento explícito y acceso controlado a las fuentes de datos.
- Minimización de datos y políticas de conservación adecuadas.
- Gestión segura de credenciales y tokens.
- Autenticación y autorización por usuario.
- Protección de datos personales en registros, trazas y conjuntos de evaluación.
- Validación de resultados generados antes de modificar el estado persistente.
- Protección frente a ataques de inyección de instrucciones en correos, mensajes y contenido externo.
- Restricción de permisos de herramientas y aprobación explícita de acciones sensibles.
- Mecanismos de acceso, rectificación, exportación y eliminación de datos.
- Transparencia sobre la incertidumbre y las limitaciones de las conclusiones generadas por IA.

Se priorizarán los datos sintéticos durante el desarrollo, las pruebas automatizadas y las demostraciones públicas.

El diseño final tendrá en cuenta los requisitos aplicables de protección de datos, incluido el RGPD cuando corresponda. El cumplimiento dependerá de la implementación y de las actividades de tratamiento efectivamente realizadas.

## 7. Áreas tecnológicas

Las siguientes tecnologías representan áreas de exploración, no una arquitectura de implementación cerrada.

| Área | Tecnologías o enfoques candidatos |
|---|---|
| Backend | Python, FastAPI, programación orientada a objetos |
| IA agéntica | Modelos de lenguaje, uso de herramientas y orquestación de flujos |
| Interoperabilidad | Model Context Protocol (MCP) |
| Memoria | Bases de datos relacionales, embeddings, búsqueda vectorial y RAG |
| Procesamiento de datos | Validación, normalización y análisis estadístico interpretable |
| Audio | Síntesis de voz y, opcionalmente, reconocimiento de voz |
| Contenedores | Docker y Docker Compose |
| CI/CD | Git, GitHub y GitHub Actions |
| Cloud | AWS o Azure |
| Infraestructura | Infraestructura como código |
| Observabilidad | Registros estructurados, trazas y métricas |
| Calidad | Pruebas automatizadas, evaluación de IA y controles de seguridad |

El proyecto podrá utilizar redes neuronales y modelos de lenguaje preentrenados cuando resulte apropiado, sin convertir el entrenamiento de modelos propios en un requisito central.

Las decisiones tecnológicas estarán guiadas por los requisitos del proyecto, el contenido del máster y el equilibrio entre calidad, complejidad, coste y mantenibilidad.

## 8. Hoja de ruta propuesta

El proyecto seguirá un enfoque incremental, priorizando una solución funcional de extremo a extremo.

**Fase 1 — Fundamentos**

Definir los casos de uso, la arquitectura, el modelo de datos, la API y el flujo de desarrollo. Preparar el repositorio, la estrategia de pruebas y los datos sintéticos.

**Fase 2 — MVP funcional**

Implementar conectores de datos simulados, normalización de eventos, persistencia, generación del diario y extracción básica de tareas.

**Fase 3 — IA agéntica y memoria**

Introducir orquestación controlada, agentes especializados seleccionados, herramientas MCP y recuperación de contexto histórico.

**Fase 4 — Insights personales**

Desarrollar análisis histórico interpretable, recomendaciones personalizadas y mecanismos de retroalimentación del usuario.

**Fase 5 — Calidad de IA y fiabilidad operativa**

Establecer conjuntos de evaluación, métricas de referencia, comprobaciones de regresión, trazabilidad, gestión de errores y monitorización de costes.

**Fase 6 — Experiencia multimodal**

Implementar la generación asíncrona de podcasts e integrar fuentes reales seleccionadas cuando sea viable.

**Fase 7 — Despliegue cloud y validación final**

Automatizar pruebas y despliegues, aprovisionar la infraestructura necesaria, validar la seguridad y la resiliencia y preparar una demostración completa de extremo a extremo.

El alcance de cada fase se concretará según la duración del proyecto, los recursos disponibles y los requisitos académicos.

## 9. Entregables esperados

El proyecto final aspira a proporcionar:

- Un repositorio de GitHub documentado y mantenible.
- Un backend funcional y una interfaz de demostración.
- Integraciones de datos simuladas y, cuando sea viable, reales.
- Un flujo de diario inteligente y extracción de tareas.
- Un prototipo de memoria histórica e insights personalizados.
- Un diario narrado en formato de audio.
- Una arquitectura de agentes controlada con integraciones MCP seleccionadas.
- Pruebas automatizadas y un benchmark de evaluación de IA.
- Una aplicación contenedorizada y desplegada en un entorno cloud.
- Un pipeline CI/CD automatizado.
- Documentación técnica sobre arquitectura, seguridad, evaluación y despliegue.
- Una demostración respaldada por resultados medibles de calidad, latencia y coste.

## 10. Criterios de éxito

dIArio se considerará satisfactorio cuando demuestre algo más que la capacidad de generar texto aparentemente convincente.

La solución final deberá ser capaz de procesar información de múltiples fuentes, producir un diario trazable, identificar posibles compromisos, recuperar contexto histórico relevante y generar un resumen narrado mediante un flujo reproducible.

La calidad se evaluará mediante pruebas funcionales, resultados de evaluación, comprobaciones de seguridad y métricas operativas.

El informe final documentará los resultados reales, las limitaciones, las decisiones de diseño y las oportunidades de mejora, en lugar de dar por completadas todas las funcionalidades previstas.

## 11. Visión a largo plazo

dIArio aspira a evolucionar desde un diario automatizado hasta convertirse en un asistente personal de IA que ayude a las personas a recordar sus experiencias, comprender sus rutinas y tomar decisiones más conscientes sobre su tiempo y sus objetivos.

La ambición del proyecto es demostrar cómo la inteligencia artificial moderna, la ingeniería de software, el cloud computing y DevOps pueden combinarse para crear una aplicación real útil, medible y responsable.

**dIArio — De los datos cotidianos a los descubrimientos personales.**
