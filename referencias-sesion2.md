# Referencias · Sesión 2 — Automatizo con la IA · Grupo Estudios

Material complementario para los asistentes. Aquí encontraréis los enlaces, conceptos y prompts que hemos visto durante la sesión, listos para copiar y reutilizar en vuestro día a día.

> Las secciones están ordenadas igual que las slides del PPTX. En cada sección aparece el **nº de slide de referencia** — podéis buscar con *Cmd+F "Slide 14"* para saltar directamente.

---

## Antes de empezar — descargad la carpeta `demos/`

Todas las demos que reproduciréis en casa usan archivos preparados que están en la carpeta [`demos/`](demos/) de este repositorio. Para seguir las prácticas **sin perder tiempo creando ficheros**, descargad toda la carpeta `demos/` a vuestro ordenador antes de la sesión.

Dentro, cada subcarpeta corresponde a una demo concreta (por ejemplo `demos/09-primera-tarea/`). A lo largo de este documento os indicaré **qué subcarpeta autorizar en Cowork** para cada caso.

Cómo descargarla:

- **Opción rápida** — clonar todo el repo:
  ```bash
  git clone https://github.com/danisev7/geinstal-ia-sesion2-estudios.git
  ```
- **Sin git** — descargar el repo como ZIP desde el botón verde *Code → Download ZIP* en GitHub y descomprimirlo.

---

## Recursos útiles

| Recurso | Enlace |
|---------|--------|
| App de escritorio Claude (Mac/Windows) | [claude.ai/download](https://claude.ai/download) |
| Web de Claude | [claude.ai](https://claude.ai) |
| Curso oficial Anthropic — *Introduction to Claude Cowork* | [anthropic.skilljar.com/introduction-to-claude-cowork](https://anthropic.skilljar.com/introduction-to-claude-cowork) |
| Directorio oficial de Plugins | [claude.com/plugins](https://claude.com/plugins) |
| Claude en Chrome (extensión, beta · Pro/Max/Team/Enterprise) | [claude.ai/chrome](https://claude.ai/chrome) |
| Usar Claude en Chrome de forma segura (prompt injection) | [support.claude.com/…/12902428](https://support.claude.com/en/articles/12902428-using-claude-in-chrome-safely) |
| Documentación de Skills (cómo escribir un SKILL.md) | [docs.claude.com/skills](https://docs.claude.com/en/docs/build-with-claude/skills) |
| Documentación de Conectores (MCP) | [modelcontextprotocol.io](https://modelcontextprotocol.io) |

> **Plan recomendado para Geinstal:** Team. Habilita Cowork, Skills compartidas, Conectores corporativos (Outlook/OneDrive/Teams) y comparte límites de uso entre el equipo. La extensión de Chrome está disponible en Pro, Max, Team y Enterprise.

---

## Qué es Cowork (en una frase) · Slide 4

> **De la conversación a la delegación.** En el chat preguntas y copias lo útil. En Cowork describes un resultado y Claude planifica, ejecuta y entrega los archivos donde se los pediste.

Construido sobre la misma arquitectura que **Claude Code** — el sistema agéntico que Anthropic usa para fabricar software de producción.

---

## Las 3 cosas que hacen posible Cowork · Slide 5

| | |
|---|---|
| **Planificar** | Antes de tocar nada, Claude muestra su plan. Tú lo revisas, ajustas, apruebas. |
| **Ejecutar** | El trabajo corre en un entorno aislado de tu ordenador. Tareas largas, sin tiempos de espera. |
| **Conectar** | Alcanza los sistemas donde vive tu trabajo: correo, Drive, calendario, herramientas conectadas. |

---

## Las 6 capacidades centrales · Slide 6

1. **Conectores** — accede a tus herramientas: correo, Drive, Slack, calendarios.
2. **Operaciones con archivos** — lee y crea archivos reales: `.docx`, `.xlsx`, `.pptx`, `.pdf`.
3. **Plugins** — especialización por rol: ventas, finanzas, legal, marketing.
4. **Tareas programadas** — tareas que se ejecutan en una cadencia recurrente.
5. **Subagentes** — trabajo paralelo: varios subagentes simultáneos.
6. **Cómputo local** — corre código sobre tus archivos en sitio, sin subir/descargar.

---

## Qué necesitas para arrancar · Slide 8

- ☑ App **Claude Desktop** (Mac/Windows, gratis)
- ☑ **Cuenta Claude con plan de pago** (Pro, Max, Team o Enterprise)
- ☑ Una **carpeta de trabajo dedicada** — NO toda la unidad ni el escritorio entero
- ☑ **Conectores** — Outlook, OneDrive, Teams (Geinstal usa Microsoft 365)
- ☑ **Claude en Chrome** (opcional, beta · disponible en Pro, Max, Team y Enterprise) — para páginas sin conector. Útil para portales como BOE, PLACE, GMAOs web.

---

## Demo — Vuestra primera tarea con Cowork · Slide 9

La demo de *"primera tarea"* que habéis visto en directo la podéis replicar vosotros mismos. Es la forma más rápida de ver el flujo end-to-end de Cowork sin riesgo (solo lee, no modifica nada).

### Carpeta a usar

`demos/09-primera-tarea/` — contiene:

| Archivo | Qué es |
|---------|--------|
| `pliego-A.pdf` | Pliego corto ficticio — Hospital de Sant Pau (3 pág) |
| `pliego-B.pdf` | Pliego corto ficticio — CCCB Barcelona (3 pág) |
| `plantilla-costes.xlsx` | Plantilla de costes internos de Geinstal (partidas HVAC, ELE, PCI, fontanería + reglas transversales) |

### Cómo reproducirla en 3 minutos

1. **Abre Claude Desktop** → cambia al modo **Cowork** → **autoriza la carpeta `demos/09-primera-tarea/`**.

2. **Lanza este prompt** en el chat:

   ```
   Léeme los archivos que hay en esta carpeta y dime qué es
   cada uno y qué información contienen.
   ```

3. **Revisa el plan** que te muestra Cowork → **Aprueba** → observa cómo lee los tres archivos en paralelo y devuelve un resumen estructurado.

> La carpeta queda **intacta**: el prompt no pide crear nada, así que Cowork no toca un solo byte. Este es el flujo base; todo lo demás que hace Cowork es una variación de estos mismos 4 pasos.

---

## El ciclo de la tarea (4 pasos oficiales) · Slide 10

1. **Describe qué quieres recibir** — qué mirar, qué devolver, dónde guardarlo.
2. **Responde a unas preguntas** — Claude afina con preguntas clave (formato, ubicación, etc.).
3. **Aléjate — o intervén** — ves el progreso, puedes redirigir en cualquier momento.
4. **Abre tu trabajo terminado** — los archivos aparecen donde los pediste.

> **Trata el resultado como un borrador.** Léelo como leerías un primer borrador de un compañero competente.

---

## Demo — De carpeta caótica a presentación ejecutiva · Slide 12

Reproduce la demo del **walkthrough oficial** de Anthropic, aterrizada a un caso de Geinstal: partir de una carpeta con documentos sueltos de una revisión de herramientas del departamento de Estudios, y pedirle a Cowork una presentación ejecutiva para dirección.

### Carpeta a usar

`demos/12-revision-herramientas/` — contiene:

| Archivo | Qué es |
|---------|--------|
| `notas-reunion-1-diagnostico.docx` | Notas de la reunión inicial de diagnóstico (qué herramientas usamos, qué falla) |
| `notas-reunion-2-priorizacion.docx` | Taller de priorización con dot-voting del equipo |
| `notas-reunion-3-it-integraciones.docx` | Reunión con IT sobre viabilidad técnica y seguridad |
| `timeline-proyecto.xlsx` | Cronograma de implantación + hoja de KPIs con gráfico |
| `analisis-previo-herramientas.pdf` | Benchmarking resumido de alternativas (Claude Team, ChatGPT, Copilot…) |
| `equipo-estudios.jpg` | Foto del equipo para la portada de la presentación |

### Cómo reproducirla

1. **Autoriza** en Cowork la carpeta `demos/12-revision-herramientas/`.

2. **Lanza este prompt**:

   ```
   Revisa todo lo que hay en esta carpeta y crea una presentación
   de 8-10 slides para la dirección sobre la revisión de herramientas
   del departamento de Estudios. Incluye:
     - Portada con la foto del equipo
     - Resumen ejecutivo
     - Estado actual (qué tenemos hoy y qué falla)
     - Propuesta priorizada con el resultado del taller
     - Cronograma del piloto
     - KPIs objetivo (con gráfico editable)
     - Próximos pasos y decisión pedida a dirección
   Guárdala como revision-herramientas-direccion.pptx.

   Antes de hacer nada muestrame el plan de lo que vas a realizar
   ```

3. **Revisa el plan** (4 pasos: leer docs → sintetizar → construir outline → generar slides) y aprueba.

4. **Abre el .pptx resultante**. Comprueba:
   - Los **gráficos son editables** (clic en el gráfico → se abren los datos nativos de PowerPoint, no es una imagen).
   - Los **datos del cronograma** provienen del Excel original.
   - La **portada** incluye la foto del equipo.

5. **Itera si hace falta**: *"cambia el título de la slide 3"*, *"añade una slide de riesgos entre estado actual y propuesta"*. Cowork edita el mismo archivo.

> Este es el ejercicio más completo de la sesión: toca **leer varios tipos de archivo**, **sintetizar en varios pasos**, **generar un archivo Office nativo**, e **iterar sobre el resultado**. El ciclo de la tarea en su forma más rica.

---

## Cómo dar contexto persistente a Cowork (3 niveles) · Slide 13

| Nivel | Dónde | Para qué |
|-------|-------|----------|
| **Usuario** | Instrucciones globales (Settings) | Preferencias que aplican siempre: rol, tono, formatos favoritos |
| **Proyecto** | Panel de instrucciones del Project | Quién participa, dónde viven las cosas, reglas del proyecto |
| **Contenido** | Archivos en la carpeta del Project | Plantillas, históricos, criterios internos |

### Ejemplo de instrucciones de Project — `Licitaciones-2026`

```
Eres mi asistente para el departamento de Estudios de Geinstal.
Geinstal es una empresa de mantenimiento integral con 305 empleados,
35M€ de facturación, especializada en HVAC, electricidad, fontanería
y PCI. Sede en Sant Cugat del Vallès.

Cuando analices pliegos:
- Cita siempre la página del pliego de la que sacas cada dato.
- Si no encuentras un dato: di "NO ESPECIFICADO" — no inventes.
- Cruza los datos con /criterios-internos/ antes de recomendar.
- Las recomendaciones deben ser una de tres: PRESENTARSE / NO
  PRESENTARSE / CON SOCIO. Nada de "depende".

Estructura de la carpeta:
- /pliegos/ — PDFs de licitaciones entrantes
- /criterios-internos/ — reglas de Geinstal sobre cuándo presentarse
- /ofertas-presentadas/ — histórico de ofertas anteriores
- /analisis/ — donde aterrizan los outputs
```

---

## Demo — Montar vuestro Project "Licitaciones-2026" · Slide 14

Montad el **Project que vais a usar en los Casos 4 y 5 del Bloque 2**. En la demo en directo se crea la carpeta desde cero; en casa os dejamos la estructura completa montada para que sólo tengáis que apuntar Cowork a ella y pegar las instrucciones.

### Carpeta a usar

`demos/14-licitaciones-2026/` — estructura de 5 subcarpetas lista para usar como Project:

```
14-licitaciones-2026/
├── pliegos/                         ← pliegos y plantillas de oferta que manda el cliente
│   ├── pliego-hospital-sant-pau.pdf
│   ├── pliego-imdea-alimentacion.pdf
│   └── oferta-ClienteX.xlsx         (plantilla pesada del cliente — se usa en la demo 17)
├── ofertas-presentadas/             ← histórico y salida de ofertas valoradas
├── plantillas/                      ← plantillas internas de Geinstal
│   ├── plantilla-memoria-tecnica.docx
│   ├── plantilla-valoracion-oferta.xlsx
│   └── costes-internos-2026.xlsx    (105 códigos Geinstal + reglas transversales)
├── criterios-internos/              ← reglas de Geinstal (cuándo presentarse, márgenes…)
│   ├── cuando-presentarse.md
│   ├── margenes-minimos.md
│   └── capacidad-actual.md
└── analisis/                        ← salida de Cowork cuando analiza pliegos
```

### Cómo reproducirla

1. **Crea un nuevo Project en Cowork** y apúntalo a la carpeta `demos/14-licitaciones-2026/`.

2. **Pega este texto en el panel de instrucciones** del Project:

   ```
   Eres mi asistente del departamento de Estudios de Geinstal.
   Geinstal es una empresa de mantenimiento integral en Sant Cugat
   del Vallès con 305 empleados y 35 M€ de facturación.

   Estructura de este Project:
   - pliegos/             → pliegos y plantillas de oferta del cliente
   - plantillas/          → plantillas internas (memoria técnica,
                            costes 2026, valoración de oferta)
   - criterios-internos/  → reglas de Geinstal (cuándo presentarse,
                            márgenes mínimos, capacidad actual)
   - ofertas-presentadas/ → histórico + ofertas valoradas (salida)
   - analisis/            → salida de análisis de pliegos

   Reglas generales:
   - Si no encuentras un dato, di "NO ESPECIFICADO" — nunca inventes.
   - Cita siempre la página del pliego cuando extraigas datos de un PDF.
   - Cruza tus decisiones con los archivos de `criterios-internos/`
     (distancia máxima, margen mínimo, capacidad del equipo).
   - No borres nada sin pedirme confirmación.

   Para ANÁLISIS de pliegos (PDF del cliente → recomendación):
   - Devuelve resumen ejecutivo + tabla de criterios + recomendación
     (una de tres: PRESENTARSE / NO PRESENTARSE / CON SOCIO).
   - Guarda el análisis en `analisis/[nombre-pliego]/`.
   - Drafts de memoria técnica en .docx, finales en PDF.

   Para VALORACIÓN de ofertas (plantilla Excel que manda el cliente):
   - Respeta la estructura original del Excel (no reordenes columnas
     ni capítulos).
   - Cruza partida por partida con `plantillas/costes-internos-2026.xlsx`.
   - Aplica el margen que te indique el prompt.
   - Partidas sin equivalente claro → déjalas vacías y lístalas en
     una hoja nueva "Sin-match".
   - Partidas ambiguas o duplicadas → hoja "Revisar".
   - Guarda la oferta valorada en `ofertas-presentadas/`.
   ```

3. **Lanza este prompt** (el "día 1 del becario" — sirve para comprobar que el Project ha cargado bien el contexto):

   ```
   Acabo de crear este Project. Léete todos los archivos que hay
   en la carpeta y dime qué tienes, para qué crees que sirve, y
   qué instrucciones seguirás. Si algo no queda claro, pregúntame.

   Antes de hacer nada muestrame el plan de lo que vas a realizar.
   ```

4. **Revisa la respuesta**: debería reconocer los 2 pliegos, los 3 archivos de `criterios-internos/`, las 2 plantillas, y entender la estructura de carpetas. Si te hace preguntas de clarificación, respóndelas.

> Con esto ya tenéis el Project listo para los Casos 4 y 5 del Bloque 2. En el Caso 4 pedimos un análisis completo del pliego de Sant Pau; en el Caso 5 encapsulamos ese análisis en una Skill reutilizable.

---

## El patrón de prompt — la receta oficial · Slide 15

```
PROMPT = ENTRADA + TRANSFORMACIÓN + SALIDA
```

| | ✗ Vago | ✓ Con patrón |
|---|---|---|
| **Prompt** | "Limpia mis archivos" | "Ordena mi carpeta Descargas por tipo de archivo en subcarpetas con fecha" |
| **Entrada** | (ninguna) | "mi carpeta Descargas" |
| **Transformación** | (ambigua) | "ordena por tipo de archivo" |
| **Salida** | (ninguna) | "en subcarpetas con fecha" |

---

## Demo — Valorar una oferta con Excel pesado · Slide 17

El caso **diario crítico de Estudios**. Todos manejáis plantillas Excel de ofertas con docenas o cientos de partidas — cada cliente con su estructura, sus códigos, sus unidades. Esta demo os enseña cómo Cowork ataca directamente ese trabajo.

> **Esta demo se hace dentro del Project `Licitaciones-2026`** que montasteis en el apartado anterior. Los dos archivos necesarios ya viven en la estructura del Project (`pliegos/` y `plantillas/`) — no hay que mover nada.

### Archivos implicados

| Archivo | Ubicación | Qué es |
|---------|-----------|--------|
| `oferta-ClienteX.xlsx` | `pliegos/` | Plantilla realista de un hospital grande (Vall d'Hebron) — **9 hojas · 177 partidas** distribuidas en Climatización, Electricidad, PCI, Fontanería, Elevadores, Equipos especiales, Personal adscrito y Mejoras. Celdas amarillas vacías a rellenar. Fórmulas de subtotal y total general ya montadas. |
| `costes-internos-2026.xlsx` | `plantillas/` | Costes internos Geinstal (**105 códigos** en 6 secciones) + hoja de *Reglas transversales* (márgenes mínimos, recargos, overhead). |

> **Deliberadamente algunas partidas de la plantilla no tienen equivalente exacto** en los costes internos (ej. *"Supervisión remota BMS con integración Gridcontrol v5"*, *"Sistema tubo neumático transporte muestras"*, *"Mantenimiento sistema aire comprimido medicinal"*). Eso fuerza que Cowork genere la hoja *"Sin-match"*.

### Cómo reproducirla

1. **Abre un chat nuevo** dentro del Project `Licitaciones-2026` (el Project ya sabe qué es `pliegos/`, `plantillas/` y `ofertas-presentadas/` porque está en sus instrucciones).

2. **Lanza este prompt**:

   ```
   Valórame la oferta que tenemos del Hospital Vall d'Hebron.

   La plantilla del cliente está en pliegos/oferta-ClienteX.xlsx.
   Tiene 9 hojas (1 resumen + 8 capítulos técnicos). Rellena en
   cada capítulo las columnas F (Precio unitario oferta) y G (Total)
   cruzando con plantillas/costes-internos-2026.xlsx.

   Instrucciones específicas de esta oferta:
   - Aplica un margen global del 18 % sobre nuestro coste interno.
   - Respeta las fórmulas =D*F y =SUM() que ya están en el Excel —
     al rellenar F, los totales y subtotales se actualizan solos.
   - Al terminar, escribe en ofertas-presentadas/ un archivo
     resumen-vallhebron.docx con: importe total anual, nº de partidas
     valoradas/sin-match/a-revisar, 5 partidas con margen más bajo
     y 5 con margen más alto, riesgos detectados.

   Guarda el Excel valorado como
   ofertas-presentadas/oferta-ClienteX-valorada.xlsx.

   Antes de hacer nada muéstrame el plan de lo que vas a realizar.
   ```

3. **Revisa el plan**: leer plantilla del cliente → leer costes → mapear capítulo por capítulo → rellenar columnas → generar hojas Sin-match y Revisar (según las reglas del Project) → guardar en `ofertas-presentadas/`. Aprueba.

4. **Abre el `.xlsx` resultante** y comprueba:
   - Los **subtotales de cada capítulo** se han calculado solos (fórmulas `=SUM(...)` actualizadas).
   - El **total general** aparece en la hoja `Resumen`.
   - La hoja **`Sin-match`** lista las partidas que Cowork no ha podido cruzar (debería incluir, al menos, las partidas singulares del hospital que no están en costes internos).
   - El **`resumen-vallhebron.md`** trae la síntesis ejecutiva.

5. **Itera**: pide *"explícame cómo has calculado el total de la partida P-HVAC-042"* y Cowork te contará qué código interno usó, qué margen aplicó y qué asunciones tomó. Cada celda es **auditable**.

> **Lección clave**: el 90 % del Excel se rellena solo. Tu trabajo como humano es revisar las partidas sin match (20-30 típicamente) y decidir el coste. **Pasas de 4 horas de copia-pega a 20 minutos de revisión técnica.**
>
> Y lo más importante: el Project `Licitaciones-2026` cubre **tanto el análisis de pliegos como la valoración de ofertas** gracias a las reglas condicionales del panel de instrucciones. Un único asistente contextualizado para todo el flujo del departamento.

---

## Conectores — donde vive vuestro trabajo · Slide 18

Anthropic mantiene **más de 38 conectores oficiales** sobre el estándar abierto **MCP (Model Context Protocol)**.

| Categoría | Conectores destacados |
|-----------|----------------------|
| **Productividad (M365 destacado)** | Outlook · OneDrive · Teams · SharePoint · Gmail · Google Drive · Calendar · Slack · Notion · Dropbox · Box |
| **Desarrollo** | GitHub · Jira · Linear · Azure DevOps |
| **CRM / Ventas** | Salesforce · HubSpot · Apollo |
| **Datos** | Snowflake · BigQuery · Databricks |
| **Legal / Documentos** | Harvey · DocuSign |

Activación: `Customize → Conectores → Authenticate`.

---

## Skills — qué son y cuándo crearlas · Slide 19

Una Skill es un **procedimiento operativo completo** escrito en Markdown: pasos en orden, instrucciones exactas, plantillas de salida, ejemplos. El *"cómo lo hacemos aquí"* de una tarea repetida, capturado en un archivo que Claude ejecuta tal cual.

### Crear una Skill cuando se cumple al menos UNO

1. **Tarea que repites** con pequeñas variaciones.
2. **Reglas internas** que siempre aplican (márgenes, formato, errores a evitar).
3. **Conocimiento en una cabeza** que quieres hacer compartible.
4. **Invocable con `/comando`** en vez de reexplicarlo cada vez.

---

## Skills — anatomía del SKILL.md · Slide 20

Una Skill vive en un archivo `SKILL.md` con dos partes: un **frontmatter** con `name` + `description` (el **disparador**) y un cuerpo con las reglas.

### Skills nativas de Cowork

`.docx` · `.xlsx` · `.pptx` · `.pdf` · Markdown. Claude las invoca solo cuando la tarea las necesita.

### El campo `description` NO es un resumen — es un disparador

Claude lo lee para decidir si activar la Skill. Tiene que dejar clarísimo **cuándo** debe usarse.

```yaml
---
name: analiza-pliego
description: Analiza un pliego de licitación de mantenimiento integral.
  Devuelve resumen ejecutivo, tabla de criterios y recomendación.
  Úsalo cuando entre un pliego nuevo en /pliegos/.
---
```

(Ver el SKILL.md completo en la sección **Caso 5** de este documento.)

---

## Plugins = Cowork especializado para tu rol · Slide 21

> **Plugin = Skills + Conectores + Subagentes empaquetados para un rol**

| Plugin | Qué incluye |
|--------|-------------|
| **Plugin de Ventas** | Skills de prospección y propuestas + conectores al CRM + subagentes por cuenta |
| **Plugin de Finanzas** | Skills de modelado + Snowflake/Excel + subagentes por escenario |
| **Plugin Legal** | Skills de revisión contractual + DocuSign + subagentes por cláusula |

Plugins de código abierto para ventas, marketing, producto, finanzas, legal, RRHH, ingeniería en el directorio oficial: [claude.com/plugins](https://claude.com/plugins).

---

## Anatomía de un Plugin · Slide 22

```
plugin-ventas/
├── plugin.json          ← manifiesto: nombre, descripción, dependencias
├── skills/              ← las Skills que trae
│   ├── preparar-llamada/
│   │   └── SKILL.md
│   ├── reporte-semanal/
│   │   └── SKILL.md
│   └── redactar-propuesta/
│       └── SKILL.md
├── connectors/          ← conectores opcionales que instala
└── commands/            ← comandos /barra (/preparar-llamada, etc.)
```

Todo texto plano. Si no te gusta cómo funciona una Skill, abres el archivo y la editas.

---

## Tareas programadas — `/schedule` · Slide 23

> **Skill = QUÉ hacer · Programación = CUÁNDO hacerlo.** Compone naturalmente.

Dos formas de crear una tarea programada:

- **Rápida** — en cualquier chat de Cowork, escribís `/schedule` y un asistente os guía.
- **UI estructurada** — en la barra lateral de Cowork hay una sección **Scheduled** donde podéis crear, editar, pausar y ver el histórico de ejecuciones de vuestras tareas.

### Ejemplos para Estudios

| Cadencia | Tarea |
|----------|-------|
| Cada **lunes 8:00** | Resumen semanal de licitaciones nuevas en portales públicos |
| Cada **viernes 17:00** | Balance de ofertas del equipo esta semana |
| **Diariamente 12:00** | Correos urgentes en Outlook + borrador de respuesta |
| **Mensualmente día 1** | Dashboard Excel con KPIs de Estudios |

---

## Demo — Gmail digest semanal (tarea programada) · Slide 24

> **Este ejemplo usa Gmail** por simplicidad (sin carga corporativa). Para reproducirlo con vuestro **Outlook de Geinstal**, reemplazad *"Gmail"* por *"Outlook"* en el prompt — el resto funciona igual con el conector Outlook.

**Paso 1 — Conectar el correo**: `Customize → Conectores → Gmail → Authenticate` (o `Outlook` si es lo vuestro).

**Paso 2 — Crear la tarea programada** desde la sección `Scheduled` de la barra lateral → *New task*. Rellenad:

- **Nombre**: `resumen-newsletters-semanal`
- **Descripción**: *Resume las newsletters de la semana en un Markdown*
- **Prompt**:

  ```
  Busca en mi Gmail las newsletters recibidas en los últimos
  7 días. Identifica tú mismo cuáles son newsletters (contenido
  periódico de empresas o autores, no correos personales ni
  transaccionales) — suelen venir de direcciones tipo
  newsletter@, info@, noreply@, o de servicios tipo Substack.

  Para cada una extrae: remitente, asunto, fecha y un resumen
  de 1-2 frases del tema principal.

  Genera un resumen en
  /Users/ironmac/Dev-local/claude-projects/Newsletters-Resumen/resumen-newsletters-YYYY-WW.md
  con:

  1. Cabecera con el rango de fechas de la semana.
  2. Top 3 temas que se repiten esta semana (análisis transversal).
  3. Los 5 enlaces más interesantes (tema concreto, no enlaces
     genéricos tipo "ver en navegador" o "desuscribirse").
  4. Listado agrupado por autor con asunto + resumen de 1-2 frases.
  ```

  > ⚠ **Importante**: en los prompts de tareas programadas **no añadáis** la coletilla *"muéstrame el plan antes de hacer nada"* que sí usamos en los prompts interactivos. Si la dejáis, Cowork mostrará el plan cuando se dispare la tarea y **se quedará esperando aprobación humana** — que nadie dará si estáis fuera o dormidos, y la tarea no se ejecutará. Las tareas programadas tienen que ser **autónomas**.

- **Project**: déjalo vacío (es personal). Si queréis aislarlo, cread un Project `Newsletters` apuntando a `~/Documentos/Newsletters-Resumen/`.
- **Frecuencia**: **Semanal · Lunes · 09:00**.

**Paso 3 — Ejecutar una vez para ver el resultado** sin esperar al lunes:

```
Ejecuta ahora la tarea resumen-newsletters-semanal que acabo de
programar para que veamos el resultado.
```

Cowork lanza el prompt, aparece el plan, aprobáis, y en un par de minutos tenéis el `.md` generado en la carpeta.

> **Patrón reutilizable**: *conector + tarea programada + archivo de salida*. Cambiad *newsletters* por *correos con pliegos adjuntos de vuestro Comercial* y la misma estructura os genera un radar semanal automatizado.

---

## Los 6 prompts tipo con los que empezar · Slide 25

Todos siguen el patrón **Entrada + Transformación + Salida**.

### Organizar lo que ya tienes

```
1. "Ordena mi carpeta Descargas por tipo de archivo en
   subcarpetas con fecha."

2. "Renombra todos los archivos de esta carpeta con un
   formato consistente de fecha-primero."

3. "Crea un informe de gastos con formato a partir de
   los recibos de esta carpeta."
```

### Crear lo que necesitas

```
4. "Construye un Excel de seguimiento de proyecto a
   partir de estas notas, con columnas de estado y
   vista resumen."

5. "Convierte estas notas de reunión en una presentación
   de slides."

6. "Combina las transcripciones y notas de esta carpeta
   en un informe formateado."
```

---

## Demo — Consolidar facturas en un Excel · Slide 25

Caso muy común: al final de cada mes os toca recopilar todas las facturas y tickets de gasto de los técnicos (combustible, peajes, materiales puntuales, dietas, subcontratas…) y meter el resumen en Excel para reporte o para SAGE. Cowork lee los PDFs, extrae los datos y genera el Excel en minutos.

> **Demo transversal a los 3 grupos**: esta misma demo la usaremos en la **Sesión 2B (Mantenimiento)** con gastos de campo y en la **Sesión 3A (Administración)** con facturas entrantes que van al ERP. Solo cambia la categorización.

### Carpeta a usar

`demos/25-informe-gastos/` — contiene:

| Archivo | Qué representa |
|---------|----------------|
| `factura-01-repsol-combustible.pdf` | Recibo de repostaje flota (IVA 21%) |
| `factura-02-abertis-peajes.pdf` | Resumen mensual de peajes (IVA 21%) |
| `factura-03-wurth-tornilleria.pdf` | Factura profesional con 6 líneas |
| `factura-04-leroy-merlin-obra.pdf` | Herramientas puntuales |
| `factura-05-salvador-escoda-hvac.pdf` | Material HVAC (importe medio-alto) |
| `factura-06-air-liquide-gases.pdf` | Gases técnicos + alquiler botellas |
| `factura-07-restaurante-dieta.pdf` | Dieta comida trabajo (IVA 10%) |
| `factura-08-saba-parking.pdf` | Parking hospital (IVA 21%) |
| `factura-09-vodafone-movil.pdf` | Factura telco empresa |
| `factura-10-epis-proteccion.pdf` | EPIs (cascos, arneses, guantes) |
| `factura-11-subcontrata-ascensores.pdf` | **Importe alto** — intervención especialista |
| `factura-12-labaqua-legionella.pdf` | Análisis Legionella |
| `factura-13-ferreteria-local.pdf` | Ticket ferretería pequeño |
| `factura-14-hotel-desplazamiento.pdf` | Hotel con 2 IVAs mezclados (10% + 21%) |
| `factura-15-ticket-ambiguo.pdf` | **Ticket con datos ilegibles** — sin IVA desglosado, nombre del bar borroso |
| `informe/` | Subcarpeta de salida — aquí aterriza el Excel generado |

Variedad deliberada: **importes entre 18 € y 2.450 €**, IVAs **21 % y 10 %** mezclados, un ticket ambiguo que obligará a Cowork a usar la hoja *Alertas* (no inventa lo que no se ve).

### Cómo reproducirla

1. **Autoriza** en Cowork la carpeta `demos/25-informe-gastos/`.

2. **Lanza este prompt**:

   ```
   Analiza todas las facturas PDF de esta carpeta y consolídalas
   en un Excel informe-gastos.xlsx dentro de la subcarpeta informe/.

   Para cada factura extrae: nº factura, fecha, proveedor, NIF/CIF,
   concepto breve, categoría (combustible, peajes, repuestos, material
   eléctrico, EPIs, restauración, telefonía, subcontratas, laboratorio,
   otros), base imponible, IVA (%), IVA (€), total.

   El Excel debe tener 4 hojas:
   1. "Gastos" — una fila por factura, ordenada por fecha.
   2. "Por categoría" — suma del total por categoría con % sobre
      el total general.
   3. "Por proveedor" — top proveedores por importe acumulado.
   4. "Alertas" — facturas que requieren revisión humana: importes
      fuera de rango, IVAs que no cuadran, datos ilegibles, conceptos
      ambiguos, fechas raras.

   Si algún dato no es legible (NIF borroso, IVA no desglosado),
   déjalo vacío y añade esa factura a "Alertas" con el motivo.
   Nunca inventes un dato.

   Antes de hacer nada, muéstrame el plan.
   ```

3. **Revisa el plan** de Cowork (leer los 15 PDFs → extraer datos → categorizar → consolidar → alertas → guardar) y aprueba.

4. **Abre `informe/informe-gastos.xlsx`** y comprueba:
   - La hoja **"Gastos"** tiene las 15 facturas ordenadas por fecha.
   - La hoja **"Por categoría"** agrupa (`combustible`, `EPIs`, `subcontratas`, etc.) con porcentajes.
   - La hoja **"Por proveedor"** destaca al top-1 (subcontrata ascensores, ~2.450 €).
   - La hoja **"Alertas"** contiene al menos la **`factura-15-ticket-ambiguo.pdf`** con motivo *"nombre del establecimiento no legible, IVA no desglosado"*.

5. **Itera**: pide *"explícame cómo has calculado el IVA de la factura 14"* (hotel con 2 IVAs) y Cowork detalla el razonamiento por línea. Cada decisión es auditable.

> **ROI del caso**: 15 facturas a 2-3 minutos cada una = 30-45 minutos manuales. Cowork lo hace en 2-3 minutos. Si recibís 60-80 facturas al mes (realista en Mantenimiento o Administración), ahorráis **2-4 horas mensuales** solo en esta tarea.

---

## Pide la señal, no un resumen · Slide 27

> Una pregunta afilada os da algo accionable. Un resumen os da un resumen.

| ❌ Prompt vago | ✓ Prompt con señal |
|----------------|-------------------|
| "Resume estas transcripciones" | "¿En qué coincidió la mayoría? ¿Quién discrepó y qué tienen en común los que discreparon?" |
| "Analiza estos datos" | "¿Qué cuentas están en riesgo según los últimos 3 meses? ¿Cuál es el patrón común?" |
| "Revisa estos artículos" | "¿Dónde se contradicen? ¿Qué afirmaciones necesitan más salvedades?" |

---

## Demo — Síntesis de investigación histórica · Slide 28

El caso más potente del Bloque 1. Cowork procesa en paralelo **8 pliegos** que habéis analizado a lo largo de un año entero, los cruza con los criterios internos del departamento, y devuelve **inteligencia accionable para dirección**: no un resumen, sino las señales que permiten decidir inversiones formativas o técnicas del próximo año.

> Esta demo se hace dentro del Project `Licitaciones-2026` (el que montasteis en el apartado anterior). Los 8 pliegos históricos y los archivos de criterios internos ya están en la estructura del Project — no hay que mover nada.

### Archivos implicados

```
14-licitaciones-2026/
├── historico-pliegos/
│   ├── pliego-hospital-sant-pau.pdf           PRESENTADO
│   ├── pliego-imdea-alimentacion.pdf          NO PRESENTADO (distancia + especialización)
│   ├── pliego-hospital-clinic.pdf             NO PRESENTADO (gases medicinales)
│   ├── pliego-sant-joan-de-deu.pdf            NO PRESENTADO (gases medicinales)
│   ├── pliego-uab-fisicas.pdf                 PRESENTADO (adjudicado)
│   ├── pliego-ayto-terrassa.pdf               PRESENTADO (adjudicado)
│   ├── pliego-mercabarna.pdf                  PRESENTADO (no adjudicado por precio)
│   ├── pliego-hospital-granollers.pdf         NO PRESENTADO (gases medicinales)
│   └── decisiones.md                          Tabla con decisión y motivo por pliego
└── criterios-internos/
    ├── cuando-presentarse.md                  (ya existente)
    ├── margenes-minimos.md                    (ya existente)
    ├── capacidad-actual.md                    (ya existente)
    └── competencias-tecnicas.md               DOMINADAS vs NO DOMINADAS
```

> **Patrón plantado deliberadamente**: 3 de los 4 pliegos rechazados lo fueron por **"gases medicinales"**. Cowork debe detectar ese patrón al hacer el análisis transversal — y eso convierte la demo en un resultado "wow" en directo.

### Cómo reproducirla

1. **Abre un chat nuevo** dentro del Project `Licitaciones-2026`.

2. **Lanza este prompt** (pide la señal, no el resumen):

   ```
   En la carpeta historico-pliegos/ hay 8 pliegos que hemos
   analizado durante los últimos 12 meses. El archivo
   historico-pliegos/decisiones.md indica qué hicimos con cada
   uno (presentar / no presentar) y el motivo.

   Cruza esos 8 pliegos con los archivos de criterios-internos/
   (especialmente competencias-tecnicas.md) y respóndeme:

   1. ¿Qué 3 requisitos técnicos aparecen con más frecuencia
      en los 8 pliegos? De ellos, ¿cuáles NO dominamos hoy según
      competencias-tecnicas.md?

   2. ¿Hay un patrón en los tipos de cliente o tipos de pliego
      donde sistemáticamente hemos decidido NO presentarnos?
      (Busca un factor común — no te limites a enumerar los
      rechazos.)

   3. Proponme 2 inversiones formativas o técnicas concretas
      para 2026 basadas en los hallazgos anteriores, con
      estimación cualitativa de impacto (cuántos pliegos del
      histórico habríamos podido ganar si ya hubiéramos tenido
      esa competencia).

   Estructura la respuesta como un documento de decisión para
   dirección: titulares, hallazgos con datos, recomendaciones
   justificadas. Guárdalo en analisis/sintesis-historica-2026.md.
   ```

3. **Observa los subagentes**. Cowork lanza ~8 subagentes en paralelo (uno por pliego) — veréis el panel de progreso con las 8 lecturas simultáneas.

4. **Revisa la respuesta**. Debe detectar:
   - 3 requisitos técnicos frecuentes (HVAC, ELE y PCI aparecen en los 8; **gases medicinales** en 3 de 8 — este es el accionable).
   - El patrón: **"de los 4 rechazos, 3 fueron por gases medicinales"**.
   - Inversión 1: formación + certificación en normativa de gases medicinales (habríamos podido ganar Clínic, SJD, Granollers — 5,8 M€ combinados).
   - Inversión 2: acuerdo con laboratorio acreditado para sala limpia ISO 7 (o equivalente).

5. **Para cerrar la demo**, pide: *"Escríbeme un correo breve dirigido al director general para presentarle estas recomendaciones en 200 palabras"*. Cowork genera el correo listo para enviar.

> **Lección**: el prompt pide **señales accionables**, no resúmenes. Cowork procesa 500+ páginas de pliegos en 2 minutos y devuelve 2 decisiones de dirección con datos. Hacer esto a mano llevaría varios días — y difícilmente se llegaría a los mismos cruces.
>
> Esta es la promesa real para Estudios: no reemplazar el pensamiento, sino **procesar el material** para que vuestro pensamiento actúe sobre información ya destilada.

---

## Las 4 fronteras de seguridad de Cowork · Slide 29

| Frontera | Qué significa |
|----------|---------------|
| 🔐 **Ejecución aislada** | El trabajo corre en entorno aislado, separado del sistema operativo |
| 📁 **Acceso controlado a archivos** | Tú decides qué carpetas ve Cowork. Sin autorización, sin acceso |
| 🌐 **Respeto de las políticas de red** | Respeta las reglas de red de tu organización. Lo restringido sigue restringido |
| 🗑️ **Borrado controlado** | El borrado permanente requiere aprobación explícita. Siempre |

> El historial de conversación de Cowork se guarda **localmente en tu máquina**, no en servidores de Anthropic.

---

## Dos hábitos que debéis tener · Slide 30

### 1. Revisar resultados

> "Abre el archivo. Comprueba un número. Sigue un hilo de razonamiento."

- Cuanto más pulido parece el resultado, más importa revisarlo.
- No firmes ni envíes sin haber abierto y leído.
- Antes de mandar a cliente: ve a la página 5, comprueba un dato contra la fuente.

### 2. Gestionar el uso

Cowork consume más cuota que chat. Tres reglas oficiales:

- **Agrupa**: varias tareas relacionadas en una sola sesión — abrir sesión tiene coste.
- **Si la tarea cabe en chat, usa chat** (gasta menos).
- **Monitoriza**: en `Settings → Usage` hay visibilidad. Míralo periódicamente.

---

## Elegir modelo — Opus, Sonnet, Haiku · Slide 31

Ajusta el modelo a la tarea. **No pongas el más potente por defecto** — Opus gasta unas 5× más que Sonnet.

| Modelo | Para qué | Ejemplos en Estudios |
|--------|----------|---------------------|
| **Opus** · razonamiento profundo | Tareas complejas, decisiones críticas | Análisis de pliego + recomendación de presentarse o no. Crear una Skill nueva. |
| **Sonnet** · equilibrio · 80% del día | El trabajo diario. Bueno, rápido, razonable en coste | Rellenar plantilla Excel. Redactar memoria. Organizar carpeta. |
| **Haiku** · rápido y económico | Tareas simples o paralelo masivo | Renombrar archivos. Clasificar correos. Resumir un único documento. |

---

## Resolución de problemas — incidencias comunes · Slide 32

| Síntoma | Qué hacer |
|---------|-----------|
| *"Cowork is preparing your workspace"* tarda | Normal. El primer arranque en una sesión es más lento porque inicializa entorno. Paciencia (10–30 s). |
| Una tarea se paró a la mitad | Normalmente es que cerraste la app. Dormir el ordenador está OK — la sesión sigue. Abre Cowork → continúa. |
| Límite de uso alcanzado | Cowork gasta más que chat. Cambia a Sonnet/Haiku si la tarea lo permite. Monitoriza `Settings → Usage`. |
| No encuentro el archivo que dijo que creó | Comprueba la carpeta autorizada. Puede haber caído en una subcarpeta distinta de la esperada. Usa el panel derecho. |

> Si algo no va, primero pregúntale a Claude: **"explícame qué hiciste"**. Suele saber dónde está el problema.

---

## Hoja de ruta — los 5 pasos oficiales · Slide 33

> *"Avanza al ritmo que te encaje. La secuencia importa más que el calendario."* — Curso oficial Anthropic

1. 🧩 **Instala un Plugin** — busca uno que encaje con tu rol, instálalo y abre un archivo de Skill para mirarlo.
2. 🎯 **Lanza algo real** — elige UNA tarea de tu trabajo. Hazla en Cowork. Itera hasta que quede bien.
3. 🛠️ **Construye una Skill** — si repites la misma cosa cada semana, conviértela en Skill.
4. ⏰ **Prográmala** — ponla en cadencia recurrente. Cada lunes a las 8, o cuando tenga sentido.
5. 🤝 **Compártela** — empaqueta para tu equipo o, en Team / Enterprise, publícala.

---

# Casos prácticos del Bloque 2

Los 5 prompts ejecutados en directo durante la sesión, listos para copiar y adaptar a vuestro propio trabajo.

---

## Caso 1 · BAJA — Organizar carpeta de licitaciones nuevas · Slides 37-39

### Prompt

```
Mira la carpeta licitaciones-entrantes/.

Para cada archivo:
1. Identifica si es un pliego, un anexo, una memoria, o
   "no sé" — déjalo en una carpeta sin-clasificar/.
2. Identifica el cliente y la fecha del documento.
3. Crea una carpeta destino con formato
   organizadas/AAAA-MM-cliente-objeto/.
4. Mueve y renombra los archivos a esa carpeta destino
   (pliego.pdf, anexo-N.pdf, memoria-base.docx).
5. Genera un index.md con un resumen de qué hay en
   cada carpeta nueva.

Antes de mover nada, muéstrame el plan completo.
```

### Anotaciones

- **Entrada**: una carpeta concreta con los archivos a clasificar.
- **Transformación**: 5 pasos numerados — clasifica, identifica, crea, mueve, indexa.
- 🛡️ **Red de seguridad**: *"Antes de mover nada, plan completo."* Nada se ejecuta sin tu OK.

### Cómo reproducirla en casa

Carpeta con 13 archivos de input preparados en `demos/38-organizar-carpeta/licitaciones-entrantes/`. Cuatro clientes distintos mezclados + tres archivos "ruido" que no son licitaciones:

- **Hospital Universitari Vall d'Hebron** (abril 2026) — `pliego_v2_FINAL.pdf`, `anexo tecnico vh.pdf`, `ANEXO 3 firmado.pdf`, `Memoria_Hospital_v3.docx`.
- **SEAT Martorell** (abril 2026) — `pliego.pdf`, `Anexo_SEAT (1).pdf`.
- **Ajuntament de Girona** (marzo 2026, catalán) — `pliego-girona-borrador.pdf`, `anexo admin girona 23abr.pdf`.
- **Universitat Pompeu Fabra** (abril 2026) — `upf-bib.pdf`, `memoria_upf.docx`.
- **Sin clasificar** (esperables en `/sin-clasificar/`) — `sin titulo.pdf` (notificación de cambio de reunión), `DOC0042.pdf` (factura de proveedor), `notif.pdf` (acta interna).

Qué verificar al ejecutar la demo:

- El plan agrupa correctamente los 4 clientes y detecta que la memoria de UPF y la de Vall d'Hebron son **memorias base**, no pliegos.
- Los tres archivos ruido van a `/sin-clasificar/` — si los clasifica como anexo es señal de que hay que darle un ejemplo negativo.
- El `index.md` final debería mencionar el expediente y la fecha de cada pliego.

---

## Caso 2 · MEDIA — Consolidar valoraciones de varios clientes · Slides 40-42

### Prompt

```
En la carpeta valoraciones-Q1/ tienes 4 Excels:
uno por cliente, cada uno con su plantilla.

Quiero un Excel consolidado valoraciones-Q1-RESUMEN.xlsx
con UNA hoja por cliente y UNA hoja "Comparativa" que tenga:

– Cliente
– Importe total ofertado
– Margen estimado (€ y %)
– Nº de partidas con margen < 5% (rojo)
– Nº de partidas con margen > 20% (verde)

Si una plantilla tiene un campo que no encuentras
(p.ej. "margen estimado" no existe en la plantilla SEAT),
déjalo vacío y avísame en un comentario en la celda.

Antes de generar el Excel, dime cómo has mapeado las
columnas de cada plantilla a los campos del consolidado.
```

### Anotaciones

- **Entrada**: 4 Excels heterogéneos en una carpeta.
- **Salida**: 5 hojas (1 por cliente + Comparativa) con 5 campos definidos.
- 🛡️ **No invenciones**: campo no encontrado → vacío + comentario en celda.
- 🔍 **Mapeo visible**: antes de generar nada, ver cómo entendió las columnas de cada plantilla.

### Cómo reproducirla en casa

Los 4 Excels de input están en `demos/41-consolidar-valoraciones/valoraciones-Q1/`. Cada uno con estructura deliberadamente distinta para que Cowork tenga que mapear:

| Archivo | Cliente | Peculiaridad pedagógica |
|---|---|---|
| `valoracion-vall-hebron-2026Q1.xlsx` | Hospital Vall d'Hebron | Plantilla completa — 20 partidas con precio, coste interno, margen € y margen %. El "caso base" que cuadra con todos los campos del consolidado. |
| `valoracion-SEAT-martorell-Q1.xlsx` | SEAT Martorell | Plantilla industrial **en inglés** (`Item #`, `Description`, `Qty`, `Unit Price`, `Total`) — **sin columna de margen**. Cowork debe dejar "Margen €/%" vacío y avisar. |
| `UAB-valoracio-Q1-2026.xlsx` | UAB Bellaterra | Cabeceras en **catalán** (`Concepte`, `Preu €/ut`, `Cost intern`, `Marge`). Mismos conceptos, vocabulario distinto. |
| `CCCB-2026Q1.xlsx` | CCCB | Plantilla pobre — 3 columnas (`Descripción`, `Total €`, `Beneficio esperado %`). Agrupa bloques, no desglosa por unidades. |

El output `valoraciones-Q1-RESUMEN.xlsx` se guarda al mismo nivel que `valoraciones-Q1/` (lo genera Cowork — está en `.gitignore`).

Qué verificar al ejecutar la demo:

- **Plan de mapeo antes de generar nada**: Cowork debe decir cómo traduce cada cabecera (`Preu €/ut` → `Precio unitario`, `Item #` → `Código partida`, etc.).
- **SEAT sin margen**: en la hoja "Comparativa" y en la hoja dedicada a SEAT, las celdas de margen deben quedar vacías con un comentario tipo *"No hay coste interno en la plantilla original — pedir a Comercial"*. Si Cowork se inventa un margen, ahí tienes el fallo.
- **CCCB**: el "beneficio esperado %" de CCCB ≠ "margen %" exactamente, pero Cowork puede asimilarlo. Debe marcarlo como *aproximación*, no como dato directo.
- **Tabla comparativa**: los conteos de partidas con margen < 5% (rojo) y > 20% (verde) deben cuadrar con lo que hay en los archivos individuales.

---

## Caso 3 · MEDIA — Claude en Chrome para portales web sin conector · Slides 43-46

> **Pre-requisito**: tener instalada la extensión [claude.ai/chrome](https://claude.ai/chrome). Está en beta y disponible en los planes Pro, Max, Team y Enterprise (desde diciembre 2025).

### ⚠ Antes de usar Chrome: el riesgo del *prompt injection*

Una web puede llevar instrucciones ocultas (texto del color del fondo, comentarios HTML, texto fuera de pantalla) que **Claude lee y obedece** como si fueran tuyas. Anthropic ha documentado tres tipos de daño:

- 🔓 **Extraer información sensible** y enviársela a un atacante
- 🗑 **Borrar archivos** importantes
- 💸 **Realizar acciones dañinas** en sitios autenticados (compras, envíos)

En Opus 4.5 la tasa de éxito del ataque baja a ~1 %, pero no a cero. **5 reglas** para trabajar seguros:

1. Empezad por **sitios de confianza** (PLACE, BOE, perfil del contratante).
2. **Revisad el plan** antes de aprobar cada acción.
3. Si Claude **se desvía** (habla de otra cosa, propone rarezas) → **parad**. Ésta es la más importante.
4. No la uséis con **información confidencial a la vista**.
5. **NUNCA**: cuentas financieras · documentos legales · datos médicos · sistemas internos sensibles.

Guía oficial: [support.claude.com/en/articles/12902428](https://support.claude.com/en/articles/12902428-using-claude-in-chrome-safely).

### Prompt

```
Estoy en la Plataforma de Contratación del Sector Público
(place.gob.es). Quiero que me extraigas las licitaciones
publicadas en los últimos 7 días que cumplan:

– Tipo: servicios (CPV de mantenimiento)
– Importe estimado: > 100.000 €
– Lugar de ejecución: Cataluña

Para cada una recoge: número expediente, órgano contratante,
objeto, importe, fecha límite presentación, link al pliego.

Guarda los resultados en
radar/place-AAAA-MM-DD.xlsx
en mi carpeta Cowork.

NO me logues con mis credenciales —
si pide login, para y avísame.
```

### Anotaciones

- **Estructura habitual**: INPUT (página PLACE) + TRANSFORMACIÓN (extraer con criterios) + OUTPUT (Excel en carpeta).
- 🚨 **Última frase crítica**: Chrome opera tu navegador real. Restricción explícita: nada de credenciales, formularios o pagos sin tu OK.
- ⚠ **Beta — sitios de confianza**: existe riesgo de *prompt injection* desde la web. Empezar por sitios institucionales (PLACE, BOE, perfiles del contratante).

### Cómo reproducirla en casa

Este caso no requiere archivos de input — se ejecuta sobre un portal web público en vivo (`place.gob.es`). Prerrequisitos y pasos:

1. **Extensión Claude en Chrome** instalada (Chrome Web Store → "Claude"). Disponible en Pro/Max/Team/Enterprise desde diciembre 2025.
2. **Abre el Project `Licitaciones-2026`** en Cowork Desktop para que el output del radar aterrice dentro del Project.
3. **Navega en Chrome a [https://contrataciondelestado.es](https://contrataciondelestado.es)** (PLACE). Filtra por *servicios* y *Cataluña* para limitar resultados de la demo.
4. **Activa la extensión** desde el icono junto a la barra de URL. Autoriza la primera vez el dominio `contrataciondelestado.es`.
5. **Pega el prompt** tal cual. Revisa el plan que Cowork propone antes de aprobar.
6. **Output esperado**: `radar/place-2026-04-21.xlsx` dentro del Project `Licitaciones-2026/` (la carpeta `radar/` ya existe con un `LEEME.md` — Cowork sólo añade el Excel).

Qué verificar al ejecutar la demo:

- **Respeta la restricción de credenciales**: si PLACE pide login en algún momento, Cowork para y avisa. No intenta rellenar ningún formulario.
- **Filtra correctamente**: sólo debería extraer licitaciones de servicios en Cataluña con importe > 100.000 € publicadas en los últimos 7 días.
- **Cita el link al pliego**: cada fila debe tener la URL real del pliego en PLACE, no una inventada.
- **Plan B**: si PLACE cambia HTML o va lento durante la formación, enseñad un vídeo grabado o usad un portal alternativo (DOGC, perfil de contratante de un hospital).

---

## Caso 4 · MEDIA-ALTA — Análisis completo de pliego dentro de un Project · Slides 47-50

> Este caso usa el Project **Licitaciones-2026** ya montado, con sus instrucciones cargadas y carpetas `criterios-internos/`, `ofertas-presentadas/` y `pliegos/`.

### Prompt

```
He metido en pliegos/ un pliego nuevo:
pliego-hospital-sant-pau.pdf

Hazme un análisis completo:

1. RESUMEN EJECUTIVO en analisis/sant-pau-resumen.md (1 pág):
   – Objeto del contrato y duración
   – Importe base de licitación
   – Tipo de contrato (servicios, obra, mixto)
   – Plazo de presentación
   – Criterios de adjudicación con ponderación

2. TABLA DE CRITERIOS en analisis/sant-pau-criterios.xlsx:
   – Criterio | Peso | Cómo se valora | Encaje Geinstal (1-5)

3. RECOMENDACIÓN al final del resumen:
   – Cruza el pliego con criterios-internos/
   – Decide: PRESENTARSE / NO PRESENTARSE / CON SOCIO
   – Justifica con datos del pliego y de los criterios

Cita siempre la página del pliego de la que sacas cada dato.
```

### Anotaciones

- **3 outputs**: tres archivos concretos en rutas concretas. Sin ambigüedad.
- **Cruza con contexto**: *"cruza con criterios-internos/"* — usa el contexto del Project, no opina de la nada.
- **Decisión, no palabrería**: una de tres opciones. Nada de "depende".
- **Cita la página**: lo que separa una IA útil de una peligrosa: cada dato verificable.

### Cómo reproducirla en casa

El Project ya está montado en `demos/14-licitaciones-2026/` con todo lo necesario. El pliego de prueba **ya existe** en `pliegos/pliego-hospital-sant-pau.pdf` — no hay que descargar nada extra.

Pasos:

1. **Abre el Project `Licitaciones-2026`** en Cowork (el panel de instrucciones ya está cargado).
2. **Verifica que `pliegos/pliego-hospital-sant-pau.pdf` existe**. La carpeta `analisis/` también está lista y vacía (sólo contiene `LEEME.md`).
3. **Abre un chat nuevo dentro del Project** y pega el prompt.
4. **Output esperado**: 2 archivos en `analisis/`:
   - `sant-pau-resumen.md` (resumen ejecutivo + recomendación al final)
   - `sant-pau-criterios.xlsx` (tabla con los criterios del pliego ponderados contra el encaje Geinstal)

Qué verificar al ejecutar la demo:

- **Citas a páginas concretas**: cada dato del resumen debe llevar "(p. N)". Si Cowork se inventa la página, se nota leyendo el PDF.
- **Coherencia con `criterios-internos/`**: la recomendación debe apoyarse en `cuando-presentarse.md`, `margenes-minimos.md` y `capacidad-actual.md`. Si el pliego tiene **gases medicinales con peso > 10%**, la recomendación correcta es **NO PRESENTARSE** o **CON SOCIO**, según los criterios ya cargados.
- **Encaje Geinstal 1-5**: en la tabla Excel, los criterios donde Geinstal tiene competencia demostrada (HVAC, PCI, ELE) deben puntuar alto; los no dominados (gases medicinales, sala limpia ISO 7) deben bajar.
- **Output en `analisis/`, no en raíz**: si Cowork deja los archivos en la raíz del Project, es que no leyó bien el prompt.

---

## Caso 5 · ALTA — Crear una Skill personalizada de Geinstal · Slides 51-56

### La Skill: `/analiza-pliego`

Analiza un pliego de licitación. Devuelve un resumen ejecutivo, una tabla de criterios con encaje Geinstal, y una recomendación PRESENTARSE / NO PRESENTARSE / CON SOCIO basada en los criterios internos del departamento.

### Tres formas de invocarla

```
/analiza-pliego pliegos/pliego-hospital-sant-pau.pdf
   → análisis completo

/analiza-pliego pliegos/pliego-imdea-alimentacion.pdf --modo rapido
   → solo resumen, sin recomendación

/analiza-pliego pliegos/pliego-seat-2026.pdf --comparar 2024-SEAT
   → vs. oferta anterior del cliente
```

### Las 3 formas de crearla en Cowork

| Vía | Ruta | Cuándo usarla |
|-----|------|---------------|
| **`/skill-creator`** (hoy) | Customize → Skills → Directorio → `/skill-creator` → ⬇ Instalar | Para crear skills nuevas desde cero — te **obliga a pensar** cada decisión. |
| **"Convertir en habilidad"** | Menú contextual del chat (⋮) → *Convertir en habilidad* | Cuando ya tienes **un chat exitoso** (p.ej. el del Caso 4) y quieres empaquetarlo como skill reutilizable. |
| **A mano** | Editor + `~/.claude/skills/<nombre>/SKILL.md` | Cuando ya sabes exactamente qué reglas y formato quieres. |

### La demo paso a paso (con `/skill-creator`)

#### Paso 0 · Prerrequisito (lo hace el formador antes)

`Customize → Skills → Directorio → Anthropic y partners → /skill-creator → ⬇ Instalar`. Instalación con 1 clic. Si el asistente aún no la tiene, se hace en directo en 10 segundos desde la UI.

#### Paso 1 · Invocar `/skill-creator` dentro del Project

Abrir Cowork, entrar al Project **Licitaciones-2026**, nuevo chat, y escribir:

```
/skill-creator
```

Cowork lee la skill oficial de Anthropic y empieza a entrevistarte.

#### Paso 2 · Responder la entrevista (chuleta conversacional)

`/skill-creator` tiene **5 fases** según su SKILL.md oficial. Cowork te va llevando por ellas en orden. No hace falta que hagas nada entre fases — solo contesta cuando pregunta. Debajo, el guion literal copiable por si quieres ir al grano.

##### Fase 1 · Captura de intención (4 preguntas base)

Cowork abre la entrevista con 4 preguntas consecutivas. Las respuestas:

**① "What should this skill enable Claude to do?"** (qué debe hacer)

> ```
> Analizar un pliego de licitación de mantenimiento integral,
> cruzarlo con los criterios internos del departamento de Estudios
> de Geinstal (carpeta criterios-internos/) y devolver:
>
> 1. Un resumen ejecutivo de una página (objeto, duración, importe,
>    plazo, criterios de adjudicación con ponderación).
> 2. Una tabla de criterios (Excel) con peso, cómo se valora y
>    encaje Geinstal (1-5).
> 3. Una recomendación taxativa: PRESENTARSE, NO PRESENTARSE, o
>    CON SOCIO, justificada con datos del pliego y de los criterios.
>
> Cada dato debe llevar la página del pliego de donde se saca.
> ```

**② "When should this skill trigger?"** (cuándo activarse, qué frases)

> ```
> Cuando el usuario esté trabajando dentro del Project
> Licitaciones-2026 y haya un pliego PDF en pliegos/, y pida:
>
> - "analiza este pliego"
> - "haz un análisis de pliego"
> - "qué opinas de este pliego"
> - "vale la pena presentarse a X"
>
> O cuando el usuario invoque directamente /analiza-pliego
> con un path a un PDF.
> ```

> ℹ️ **Ojo con el "pushy"**: el SKILL.md oficial recomienda que la descripción de activación sea **un poco insistente** — incluir contextos donde la skill debería usarse aunque el usuario no lo pida explícitamente. Para evitar el sub-trigger (que no se active cuando debería), di algo como: *"Actívate también si el usuario pega o abre un PDF en pliegos/, sin pedir análisis, porque lo primero que querrá es un resumen."*

**③ "What's the expected output format?"** (formato de salida)

> ```
> Tres archivos en analisis/[nombre-pliego]/:
>
> - resumen.md   → texto, 1 página, con citas (p. N) en cada dato.
> - criterios.xlsx → tabla con columnas
>   Criterio | Peso | Cómo se valora | Encaje Geinstal (1-5).
> - recomendacion.md → PRESENTARSE / NO PRESENTARSE / CON SOCIO,
>   con 3-5 líneas de justificación y referencia al archivo de
>   criterios-internos/ que la respalda.
> ```

**④ "Should we set up test cases?"** (¿quieres casos de prueba?)

> **Sí.** Un pliego produce un output objetivamente verificable (recomendación taxativa + citas de página), así que los evals tienen sentido.

##### Fase 2 · Entrevista de investigación

Cowork profundiza sobre casos límite, formatos, dependencias. Suele preguntar:

- *"¿Hay un archivo-ejemplo del pliego que puedas mostrarme?"* → Pásale `pliegos/pliego-hospital-sant-pau.pdf`.
- *"¿Hay una carpeta o archivo con las reglas de negocio del departamento?"* → `criterios-internos/` entera; especialmente `cuando-presentarse.md`, `margenes-minimos.md` y `competencias-tecnicas.md`.
- *"¿Qué pasa si el pliego es muy largo o en otro idioma (catalán)?"* → Responde que debe leerlo igual; el catalán forma parte del trabajo normal.
- *"¿Qué dato es el más crítico que nunca debe faltar?"* → La **fecha límite de presentación** y el **importe base de licitación**.
- *"¿Hay una plantilla de entregable?"* → Si no tienes ninguna, dile que genere una `plantilla.md` con la estructura de `resumen.md` y que la use siempre.

Si Cowork te pide **reglas duras**, dale estas:

> ```
> - Cada dato del resumen tiene que llevar cita (p. N).
> - Dato no encontrado = "NO ESPECIFICADO". Nunca inventar.
> - La recomendación es UNA de tres. Nada de "depende".
> - Si el margen estimado < margen mínimo de
>   criterios-internos/margenes-minimos.md → NO PRESENTARSE,
>   aunque el resto de criterios sea favorable.
> - Si el pliego tiene peso > 10% en una competencia marcada como
>   "NO DOMINADA" en competencias-tecnicas.md → NO PRESENTARSE
>   o CON SOCIO, no PRESENTARSE en solitario.
> ```

Si Cowork te pide **errores típicos a evitar**:

> ```
> - No copiar texto literal del pliego — sintetiza con tus palabras.
> - Nada de "tal vez podríamos", "sería posible" — sé taxativo.
> - No olvidar la fecha límite — destacada arriba del resumen.
> - Si no hay margen estimado en el pliego, calcularlo cruzando
>   con plantillas/costes-internos-2026.xlsx. No dejarlo en blanco.
> ```

##### Fase 3 · Escritura del SKILL.md

Cowork propone un borrador del `SKILL.md` (nombre + description + cuerpo). **Valida dos cosas críticas**:

1. **`name: analiza-pliego`** — sin mayúsculas ni espacios. Es lo que usarás como comando.
2. **`description`** — debe mencionar *"pliego de licitación"*, *"mantenimiento integral"* y alguna frase de activación. Si la descripción es tímida, pídele que la reescriba más "pushy" — *"Actívate siempre que haya un PDF en pliegos/ y el usuario vaya a trabajar con él"*.

Si alguna **regla dura o error típico** no ha llegado al SKILL.md, pídele que los añada literalmente.

##### Fase 4 · Casos de prueba (evals)

Cowork propone 2-3 prompts realistas. Respuestas tipo:

- **Prompt 1** — *"analiza pliegos/pliego-hospital-sant-pau.pdf"*.<br>
  Expected: recomendación PRESENTARSE porque es hospital estándar en Cataluña, sin gases medicinales con peso alto. Fecha límite visible en la primera línea del resumen.
- **Prompt 2** — *"analiza pliegos/pliego-imdea-alimentacion.pdf"*.<br>
  Expected: recomendación **NO PRESENTARSE** por dos motivos: (a) IMDEA está en Madrid, > 100 km (incumple proximidad de `cuando-presentarse.md`) y (b) requiere sala limpia ISO 7 (competencia NO dominada en `competencias-tecnicas.md`).
- **Prompt 3** — *"qué opinas de este pliego"* (adjuntando el PDF de Sant Pau sin dar contexto).<br>
  Expected: la skill se activa sola (el "pushy" de la `description` hace su trabajo) y genera el análisis sin que haya que invocar `/analiza-pliego` explícitamente.

##### Fase 5 · Elegir scope y guardar

Cowork finalmente pregunta dónde colocar la carpeta de la skill. **Elige `Project`** (`<project>/.claude/skills/analiza-pliego/`). Justificación para la clase: *"Así el criterio del departamento de Estudios viaja con el Project Licitaciones-2026. Si compartimos el repositorio del Project con el equipo, la skill va incluida."*

Cowork genera la estructura completa:

```
.claude/skills/analiza-pliego/
├── SKILL.md                    ← archivo principal
├── evals/
│   └── evals.json              ← los 3 prompts con expected_output
├── ejemplos/
│   └── bueno.md                ← análisis del Sant Pau (si lo pasaste)
└── plantilla.md                ← estructura del entregable
```

#### Paso 4 · Invocar la Skill con un pliego distinto

Probar con un pliego que **no** hayas usado en el Caso 4:

```
/analiza-pliego pliegos/pliego-imdea-alimentacion.pdf
```

**Resultado esperado**: la skill debe recomendar **NO PRESENTARSE** citando al menos:

- **Distancia** — IMDEA Alimentación está en Madrid, > 100 km de Sant Cugat (incumple regla de proximidad de `cuando-presentarse.md`).
- **Sala limpia ISO 7** — competencia no dominada según `competencias-tecnicas.md`.

Si aplica esas dos reglas correctamente, la **"regla del director"** está encapsulada.

#### Paso 5 · Promover a Usuario (scope global)

En terminal, mostrar cómo copiar la skill a nivel usuario para usarla en cualquier Project:

```bash
cp -R demos/14-licitaciones-2026/.claude/skills/analiza-pliego \
      ~/.claude/skills/
```

A partir de aquí `/analiza-pliego` funciona desde **cualquier Project**, no solo Licitaciones-2026.

#### Paso 6 · Mencionar "Convertir en habilidad" como atajo

Volver al chat del Caso 4 (el análisis del Hospital Sant Pau). En el menú contextual (⋮ junto al título del chat) está la opción **"Convertir en habilidad"**. Mostrarla, no ejecutarla. *"Para la próxima vez que tengáis un chat que os encante, éste es el atajo — Cowork captura todo el flujo y lo empaqueta como skill."*

### Project vs Usuario

| Scope | Path | Alcance | Versionable | Ideal para |
|-------|------|---------|-------------|------------|
| **Project** | `<project>/.claude/skills/analiza-pliego/` | Solo en este Project | Sí (con git) | Criterio específico del departamento que viaja con el Project |
| **Usuario** | `~/.claude/skills/analiza-pliego/` | Todos tus Projects | No (local) | Skills personales que quieres tener siempre disponibles |

**Promoción Project → Usuario**: `cp -R` de la carpeta. No hay automatización oficial. **No hay promoción Usuario → Project** porque perderías el scope global; si quieres que una skill tuya la use todo el equipo, súbela al Project.

### El SKILL.md resultante

Esto es lo que `/skill-creator` genera al final (contenido equivalente; la redacción exacta puede variar):

```markdown
---
name: analiza-pliego
description: Analiza un pliego de licitación de
  mantenimiento integral. Devuelve resumen ejecutivo,
  tabla de criterios y recomendación. Úsalo cuando
  entre un pliego nuevo en pliegos/.
---

## QUÉ HACE

Toma un PDF de pliego, lo cruza con los criterios
internos del Project, y devuelve tres archivos:
resumen.md, criterios.xlsx, recomendacion.md.

## CÓMO LO HACE

1. Lee el pliego de principio a fin.
2. Consulta criterios-internos/ para conocer las
   reglas de Geinstal sobre cuándo presentarse.
3. Consulta ofertas-presentadas/ por si hay similar.
4. Genera los tres archivos en analisis/[nombre]/.

## REGLAS DURAS

– Cada dato del resumen debe tener su cita (página).
– Si no encuentras un dato: "NO ESPECIFICADO" — no inventes.
– La recomendación debe ser una de tres, no "depende".
– Si margen estimado < margen mínimo de criterios,
  NO PRESENTARSE, sin importar lo demás.

## ERRORES TÍPICOS A EVITAR

– No copiar texto literal del pliego — síntesis.
– Nada de "tal vez podríamos" — sé taxativo.
– No olvidar la fecha límite — destacada arriba.

## FORMATO DE SALIDA

Ver plantilla.md
```

### Las 4 zonas críticas del SKILL.md

- **`description`** → el **disparador**. Claude lo lee para decidir activar la Skill.
- **Reglas duras** → lo más importante. **Evita que la IA se vaya por las ramas.**
- **La regla del director** → *"Si margen < mínimo → NO"*. Encapsula una regla que solo estaba en la cabeza del director de Estudios.
- **Errores típicos** → lo aprendes iterando. Cuando algo sale mal, lo añades aquí.

---

## Deberes para la Sesión 3 · Slide 57

| Nivel | Tarea | Tiempo |
|-------|-------|--------|
| ☐ **Mínimo** | Instalar Cowork y darle permisos a una carpeta de prueba | 15 min |
| ☐ **Recomendado** | Repetir el **Caso 1** con vuestra propia carpeta de Descargas | 30 min |
| ☐ **Ambicioso** | Crear vuestro propio Project *"Mi-Trabajo-2026"* con sus instrucciones y archivos de contexto | 1 h |
| ★ **Bonus** | Identificar **1 tarea que repetís cada semana** y pensar cómo sería la Skill — la diseñamos juntos en Sesión 3 | — |

> **El bonus es lo que más impacto tiene.** Llevadlo pensado a la Sesión 3 (28 abril) para diseñar la Skill juntos.

---

## Soporte después de la sesión

Si os quedáis bloqueados con cualquier cosa, escribidme y lo vemos. La curva de aprendizaje es real las primeras dos semanas — después se nota muchísimo.

**Próxima sesión** — Nivel 3A · *Los agentes de IA trabajan por ti* (Estudios) · **28 abril 2026**.
