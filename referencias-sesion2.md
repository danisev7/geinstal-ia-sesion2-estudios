# Referencias · Sesión 2 — Automatizo con la IA · Grupo Estudios

Material complementario para los asistentes. Aquí encontraréis los enlaces, conceptos y prompts que hemos visto durante la sesión, listos para copiar y reutilizar en vuestro día a día.

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

## Conoce Claude Cowork

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

## Qué es Cowork (en una frase)

> **De la conversación a la delegación.** En el chat preguntas y copias lo útil. En Cowork describes un resultado y Claude planifica, ejecuta y entrega los archivos donde se los pediste.

Construido sobre la misma arquitectura que **Claude Code** — el sistema agéntico que Anthropic usa para fabricar software de producción.

### Las 3 cosas que lo hacen posible

| | |
|---|---|
| **Planificar** | Antes de tocar nada, Claude muestra su plan. Tú lo revisas, ajustas, apruebas. |
| **Ejecutar** | El trabajo corre en un entorno aislado de tu ordenador. Tareas largas, sin tiempos de espera. |
| **Conectar** | Alcanza los sistemas donde vive tu trabajo: correo, Drive, calendario, herramientas conectadas. |

### Las 6 capacidades centrales

1. **Conectores** — accede a tus herramientas: correo, Drive, Slack, calendarios.
2. **Operaciones con archivos** — lee y crea archivos reales: `.docx`, `.xlsx`, `.pptx`, `.pdf`.
3. **Plugins** — especialización por rol: ventas, finanzas, legal, marketing.
4. **Tareas programadas** — tareas que se ejecutan en una cadencia recurrente.
5. **Subagentes** — trabajo paralelo: varios subagentes simultáneos.
6. **Cómputo local** — corre código sobre tus archivos en sitio, sin subir/descargar.

---

## Qué necesitas para arrancar

- ☑ App **Claude Desktop** (Mac/Windows, gratis)
- ☑ **Cuenta Claude con plan de pago** (Pro, Max, Team o Enterprise)
- ☑ Una **carpeta de trabajo dedicada** — NO toda la unidad ni el escritorio entero
- ☑ **Conectores** — Outlook, OneDrive, Teams (Geinstal usa Microsoft 365)
- ☑ **Claude en Chrome** (opcional, beta · disponible en Pro, Max, Team y Enterprise) — para páginas sin conector. Útil para portales como BOE, PLACE, GMAOs web.

---

## Vuestra primera tarea con Cowork (para reproducir en casa)

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

## El ciclo completo — de carpeta caótica a presentación ejecutiva (reproducir en casa)

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

## Montar vuestro Project "Licitaciones-2026" (reproducir en casa)

Montad el **Project que vais a usar en los Casos 4 y 5 del Bloque 2**. En la demo en directo se crea la carpeta desde cero; en casa os dejamos la estructura completa montada para que sólo tengáis que apuntar Cowork a ella y pegar las instrucciones.

### Carpeta a usar

`demos/14-licitaciones-2026/` — estructura de 5 subcarpetas lista para usar como Project:

```
14-licitaciones-2026/
├── pliegos/                    ← PDFs de licitaciones entrantes
│   ├── pliego-hospital-sant-pau.pdf
│   └── pliego-imdea-alimentacion.pdf
├── ofertas-presentadas/        ← histórico (vacío en la demo)
├── plantillas/
│   ├── plantilla-memoria-tecnica.docx
│   └── plantilla-valoracion-oferta.xlsx
├── criterios-internos/         ← reglas de Geinstal escritas
│   ├── cuando-presentarse.md
│   ├── margenes-minimos.md
│   └── capacidad-actual.md
└── analisis/                   ← salida de Cowork (vacía)
```

### Cómo reproducirla

1. **Crea un nuevo Project en Cowork** y apúntalo a la carpeta `demos/14-licitaciones-2026/`.

2. **Pega este texto en el panel de instrucciones** del Project:

   ```
   Eres mi asistente del departamento de Estudios de Geinstal. Geinstal
   es una empresa de mantenimiento integral en Sant Cugat del Vallès con
   305 empleados y 35 M€ de facturación.

   Cuando analices pliegos:
   - Cita siempre la página del pliego de la que sacas cada dato.
   - Cruza siempre tus recomendaciones con los archivos de
     `criterios-internos/`.
   - Drafts de memoria en .docx, finales en PDF.
   - Guarda los análisis en la subcarpeta `analisis/`.
   - No borres nada sin pedirme confirmación.
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

## El ciclo de la tarea (4 pasos oficiales)

1. **Describe qué quieres recibir** — qué mirar, qué devolver, dónde guardarlo.
2. **Responde a unas preguntas** — Claude afina con preguntas clave (formato, ubicación, etc.).
3. **Aléjate — o intervén** — ves el progreso, puedes redirigir en cualquier momento.
4. **Abre tu trabajo terminado** — los archivos aparecen donde los pediste.

> **Trata el resultado como un borrador.** Léelo como leerías un primer borrador de un compañero competente.

---

## El patrón de prompt — la receta oficial

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

## Cómo dar contexto persistente a Cowork (3 niveles)

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

## Conectores — donde vive vuestro trabajo

Anthropic mantiene **más de 38 conectores oficiales** sobre el estándar abierto **MCP (Model Context Protocol)**.

| Categoría | Conectores destacados |
|-----------|----------------------|
| **Productividad (M365 destacado)** | Outlook · OneDrive · Teams · SharePoint · Gmail · Google Drive · Calendar · Slack · Notion · Dropbox · Box |
| **Desarrollo** | GitHub · Jira · Linear · Azure DevOps |
| **CRM / Ventas** | Salesforce · HubSpot · Apollo |
| **Datos** | Snowflake · BigQuery · Databricks |
| **Legal / Documentos** | Harvey · DocuSign |

Activación: `Settings → Connectors → Authenticate`.

---

## Skills — cómo Claude sabe cuándo usarlas

Una **Skill** es una instrucción reutilizable que vive en un archivo `SKILL.md`. Tiene dos partes: un frontmatter con `name` + `description` (el **disparador**) y un cuerpo con las reglas.

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

## Plugins = Cowork especializado para tu rol

> **Plugin = Skills + Conectores + Subagentes empaquetados para un rol**

| Plugin | Qué incluye |
|--------|-------------|
| **Plugin de Ventas** | Skills de prospección y propuestas + conectores al CRM + subagentes por cuenta |
| **Plugin de Finanzas** | Skills de modelado + Snowflake/Excel + subagentes por escenario |
| **Plugin Legal** | Skills de revisión contractual + DocuSign + subagentes por cláusula |

Plugins de código abierto para ventas, marketing, producto, finanzas, legal, RRHH, ingeniería en el directorio oficial: [claude.com/plugins](https://claude.com/plugins).

### Anatomía de un Plugin

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

## Tareas programadas — `/schedule`

> **Skill = QUÉ hacer · Programación = CUÁNDO hacerlo.** Compone naturalmente.

Activación: comando `/schedule` en Cowork. Ejemplos para Estudios:

| Cadencia | Tarea |
|----------|-------|
| Cada **lunes 8:00** | Resumen semanal de licitaciones nuevas en portales públicos |
| Cada **viernes 17:00** | Balance de ofertas del equipo esta semana |
| **Diariamente 12:00** | Correos urgentes en Outlook + borrador de respuesta |
| **Mensualmente día 1** | Dashboard Excel con KPIs de Estudios |

---

## Los 6 prompts tipo con los que empezar

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

## Pide la señal, no un resumen

> Una pregunta afilada os da algo accionable. Un resumen os da un resumen.

| ❌ Prompt vago | ✓ Prompt con señal |
|----------------|-------------------|
| "Resume estas transcripciones" | "¿En qué coincidió la mayoría? ¿Quién discrepó y qué tienen en común los que discreparon?" |
| "Analiza estos datos" | "¿Qué cuentas están en riesgo según los últimos 3 meses? ¿Cuál es el patrón común?" |
| "Revisa estos artículos" | "¿Dónde se contradicen? ¿Qué afirmaciones necesitan más salvedades?" |

---

## Las 4 fronteras de seguridad de Cowork

| Frontera | Qué significa |
|----------|---------------|
| 🔐 **Ejecución aislada** | El trabajo corre en entorno aislado, separado del sistema operativo |
| 📁 **Acceso controlado a archivos** | Tú decides qué carpetas ve Cowork. Sin autorización, sin acceso |
| 🌐 **Respeto de las políticas de red** | Respeta las reglas de red de tu organización. Lo restringido sigue restringido |
| 🗑️ **Borrado controlado** | El borrado permanente requiere aprobación explícita. Siempre |

> El historial de conversación de Cowork se guarda **localmente en tu máquina**, no en servidores de Anthropic.

---

## Dos hábitos que debéis tener

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

## Elegir modelo — Opus, Sonnet, Haiku

Ajusta el modelo a la tarea. **No pongas el más potente por defecto** — Opus gasta unas 5× más que Sonnet.

| Modelo | Para qué | Ejemplos en Estudios |
|--------|----------|---------------------|
| **Opus** · razonamiento profundo | Tareas complejas, decisiones críticas | Análisis de pliego + recomendación de presentarse o no. Crear una Skill nueva. |
| **Sonnet** · equilibrio · 80% del día | El trabajo diario. Bueno, rápido, razonable en coste | Rellenar plantilla Excel. Redactar memoria. Organizar carpeta. |
| **Haiku** · rápido y económico | Tareas simples o paralelo masivo | Renombrar archivos. Clasificar correos. Resumir un único documento. |

---

# Casos prácticos del Bloque 2

Los 5 prompts ejecutados en directo durante la sesión, listos para copiar y adaptar a vuestro propio trabajo.

---

## Caso 1 · BAJA — Organizar carpeta de licitaciones nuevas

### Prompt

```
Mira la carpeta /Descargas/licitaciones-entrantes/.

Para cada archivo:
1. Identifica si es un pliego, un anexo, una memoria, o
   "no sé" — déjalo en una carpeta /sin-clasificar.
2. Identifica el cliente y la fecha del documento.
3. Crea una carpeta destino con formato
   /Licitaciones-2026/AAAA-MM-cliente-objeto/.
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

---

## Caso 2 · MEDIA — Consolidar valoraciones de varios clientes

### Prompt

```
En la carpeta /valoraciones-Q1/ tienes 4 Excels:
uno por cliente, cada uno con su plantilla.

Quiero un Excel consolidado /valoraciones-Q1-RESUMEN.xlsx
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

---

## Caso 3 · MEDIA — Claude en Chrome para portales web sin conector

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
/Licitaciones-2026/radar/place-AAAA-MM-DD.xlsx
en mi carpeta Cowork.

NO me logues con mis credenciales —
si pide login, para y avísame.
```

### Anotaciones

- **Estructura habitual**: INPUT (página PLACE) + TRANSFORMACIÓN (extraer con criterios) + OUTPUT (Excel en carpeta).
- 🚨 **Última frase crítica**: Chrome opera tu navegador real. Restricción explícita: nada de credenciales, formularios o pagos sin tu OK.
- ⚠ **Beta — sitios de confianza**: existe riesgo de *prompt injection* desde la web. Empezar por sitios institucionales (PLACE, BOE, perfiles del contratante).

---

## Caso 4 · MEDIA-ALTA — Análisis completo de pliego dentro de un Project

> Este caso usa el Project **Licitaciones-2026** ya montado, con sus instrucciones cargadas y carpetas `/criterios-internos/`, `/ofertas-presentadas/` y `/pliegos/`.

### Prompt

```
He metido en /pliegos/ un pliego nuevo:
Hospital-Sant-Pau-2026.pdf

Hazme un análisis completo:

1. RESUMEN EJECUTIVO en /analisis/Sant-Pau-resumen.md (1 pág):
   – Objeto del contrato y duración
   – Importe base de licitación
   – Tipo de contrato (servicios, obra, mixto)
   – Plazo de presentación
   – Criterios de adjudicación con ponderación

2. TABLA DE CRITERIOS en /analisis/Sant-Pau-criterios.xlsx:
   – Criterio | Peso | Cómo se valora | Encaje Geinstal (1-5)

3. RECOMENDACIÓN al final del resumen:
   – Cruza el pliego con /criterios-internos/
   – Decide: PRESENTARSE / NO PRESENTARSE / CON SOCIO
   – Justifica con datos del pliego y de los criterios

Cita siempre la página del pliego de la que sacas cada dato.
```

### Anotaciones

- **3 outputs**: tres archivos concretos en rutas concretas. Sin ambigüedad.
- **Cruza con contexto**: *"cruza con /criterios-internos/"* — usa el contexto del Project, no opina de la nada.
- **Decisión, no palabrería**: una de tres opciones. Nada de "depende".
- **Cita la página**: lo que separa una IA útil de una peligrosa: cada dato verificable.

---

## Caso 5 · ALTA — Crear una Skill personalizada de Geinstal

### La Skill: `/analiza-pliego`

Analiza un pliego de licitación. Devuelve un resumen ejecutivo, una tabla de criterios con encaje Geinstal, y una recomendación PRESENTARSE / NO PRESENTARSE / CON SOCIO basada en los criterios internos del departamento.

### Tres formas de invocarla

```
/analiza-pliego pliegos/Hospital-Sant-Pau.pdf
   → análisis completo

/analiza-pliego pliegos/UAB-Bellaterra.pdf --modo rapido
   → solo resumen, sin recomendación

/analiza-pliego pliegos/SEAT-2026.pdf --comparar 2024-SEAT
   → vs. oferta anterior del cliente
```

### El SKILL.md completo

Guardar como `~/skills/analiza-pliego/SKILL.md`:

```markdown
---
name: analiza-pliego
description: Analiza un pliego de licitación de
  mantenimiento integral. Devuelve resumen ejecutivo,
  tabla de criterios y recomendación. Úsalo cuando
  entre un pliego nuevo en /pliegos/.
---

## QUÉ HACE

Toma un PDF de pliego, lo cruza con los criterios
internos del Project, y devuelve tres archivos:
resumen.md, criterios.xlsx, recomendacion.md.

## CÓMO LO HACE

1. Lee el pliego de principio a fin.
2. Consulta /criterios-internos/ para conocer las
   reglas de Geinstal sobre cuándo presentarse.
3. Consulta /ofertas-presentadas/ por si hay similar.
4. Genera los tres archivos en /analisis/[nombre]/.

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

Ver /skills/analiza-pliego/plantilla.md
```

### Las 4 zonas críticas del SKILL.md

- **`description`** → el **disparador**. Claude lo lee para decidir activar la Skill.
- **Reglas duras** → lo más importante. Evita que la IA se vaya por las ramas.
- **La regla del director** → *"Si margen < mínimo → NO"*. Encapsula una regla que solo estaba en su cabeza.
- **Errores típicos** → lo aprendes iterando. Cuando algo sale mal, lo añades aquí.

---

## Resolución de problemas — incidencias comunes

| Síntoma | Qué hacer |
|---------|-----------|
| *"Cowork is preparing your workspace"* tarda | Normal. El primer arranque en una sesión es más lento porque inicializa entorno. Paciencia (10–30 s). |
| Una tarea se paró a la mitad | Normalmente es que cerraste la app. Dormir el ordenador está OK — la sesión sigue. Abre Cowork → continúa. |
| Límite de uso alcanzado | Cowork gasta más que chat. Cambia a Sonnet/Haiku si la tarea lo permite. Monitoriza `Settings → Usage`. |
| No encuentro el archivo que dijo que creó | Comprueba la carpeta autorizada. Puede haber caído en una subcarpeta distinta de la esperada. Usa el panel derecho. |

> Si algo no va, primero pregúntale a Claude: **"explícame qué hiciste"**. Suele saber dónde está el problema.

---

## Hoja de ruta — los 5 pasos oficiales

> *"Avanza al ritmo que te encaje. La secuencia importa más que el calendario."* — Curso oficial Anthropic

1. 🧩 **Instala un Plugin** — busca uno que encaje con tu rol, instálalo y abre un archivo de Skill para mirarlo.
2. 🎯 **Lanza algo real** — elige UNA tarea de tu trabajo. Hazla en Cowork. Itera hasta que quede bien.
3. 🛠️ **Construye una Skill** — si repites la misma cosa cada semana, conviértela en Skill.
4. ⏰ **Prográmala** — ponla en cadencia recurrente. Cada lunes a las 8, o cuando tenga sentido.
5. 🤝 **Compártela** — empaqueta para tu equipo o, en Team / Enterprise, publícala.

---

## Deberes para la Sesión 3

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
