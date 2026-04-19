# .claude/skills/

Carpeta de **salida** para las Skills del Project `Licitaciones-2026`.

Empieza vacía (salvo este LEEME). Cuando ejecutéis la demo del **Caso 5** y `/skill-creator` os pregunte dónde guardar la skill, elegir **Project**: aquí aterrizará la estructura completa:

```
.claude/skills/analiza-pliego/
├── SKILL.md           ← archivo principal
├── ejemplos/
│   └── bueno.md       ← análisis que os gustó (p.ej. el del Caso 4)
└── plantilla.md       ← estructura del entregable
```

A partir de ese momento, dentro del Project podéis invocar `/analiza-pliego <pliego>.pdf` y Cowork aplicará todas las reglas que capturasteis en la entrevista.

**Scope**: esta carpeta hace que la skill **solo funcione dentro del Project Licitaciones-2026**. Si la queréis disponible en todos los Projects, copiadla a `~/.claude/skills/` con `cp -R`.
