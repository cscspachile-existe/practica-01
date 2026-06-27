# AGENTS.md — Contexto del proyecto

> Copia este archivo a la raíz de cada proyecto y complétalo.
> Lo leen: Cursor, Cline, Continue, Dev Muscle.

## Stack

- **Frontend:** HTML estático + React/TypeScript + Tailwind (práctica)
- **Backend:** —
- **Base de datos:** —
- **Deploy:** —

## Convenciones

- Idioma UI: español
- Idioma código/comentarios: inglés
- Estilo de nombres: PascalCase componentes, camelCase funciones
- Linter/formatter: TypeScript estricto (ver `conventions.mdc`)

## Patrones implementados

### HTML de práctica

- Páginas: `index.html`, `about.html`, `contact.html`
- CSS inline, fondo `#1a1a2e`, copy en español
- Ver `.cursor/rules/html-practica.mdc`

### Componentes UI

- `Button` con variantes `primary` / `secondary` en `src/components/Button.tsx`
- Ver `.cursor/rules/button-component.mdc`

### Autenticación

- Pendiente — escalar a Cursor cloud (Auto OFF, MAX OFF, Sonnet) si se implementa JWT
- Tras resolver: documentar en `.cursor/rules/auth-jwt.mdc`

### API

- (pendiente — REST + Zod cuando aplique)

## Enrutamiento local (0 créditos)

| Tarea | Herramienta | Rule / contexto |
|-------|-------------|-----------------|
| Preguntar, explicar convenciones | **Continue** chat | `@AGENTS.md` |
| Buscar en repo | **Continue** `@Codebase` | embed local |
| Editar HTML/TSX seleccionado | **Continue** Edit (`Ctrl+I`) | `html-practica.mdc`, `button-component.mdc` |
| Autocomplete al escribir | **Continue** Tab | `qwen2.5-coder:1.5b` |
| Crear/editar archivos nuevos | **Cline** Plan→Act | Rules en `.cursor/rules/` |
| JWT, auth, arquitectura nueva | **Cursor Agent** cloud | Solo escalación |

**No usar Agent** para HTML, Button, about/contact — ya hay Rules documentadas.

## Validación sistema híbrido (2026-06-27)

| Prueba | Herramienta | Validado en | Estado |
|--------|-------------|-------------|--------|
| Ollama API `11434` | Terminal | Terminal | OK (4 modelos) |
| Prompt "OK local" | Ollama `qwen-coder-32k` | Terminal | OK |
| Cline provider | Ollama `qwen-coder-32k` | Config | OK |
| Chat `@AGENTS.md` | Continue + Ollama | Ollama local | OK — 3 bullets convenciones |
| `@Codebase` Button | Continue + embed | Ollama local | OK — primary/secondary en `Button.tsx` |
| Edit HTML (emoji h1) | Continue Edit | Ollama local | OK — `index.html` actualizado |
| Autocomplete Tab | Continue 1.5B | Ollama local | OK — `qwen2.5-coder:1.5b` responde |
| Embed `@Codebase` | `nomic-embed-text` | Ollama local | OK |
| Crear/editar HTML | Cline / Agent | Agent cloud | OK (repetir en Cline panel) |
| Button.tsx | Cline / Agent | Agent cloud | OK |
| Rules html-practica | about.html, contact.html | Cline/Agent | OK |
| Preview HTML | Archivo directo | Navegador | OK (no `localhost:5600`) |

> **Nota:** Pruebas Continue validadas vía Ollama local (`localhost:11434`). Repetir en **panel Continue** para confirmación UI end-to-end (0 créditos).

## Estructura del repo

```
/
├── index.html
├── about.html
├── contact.html
├── src/
│   └── components/
│       └── Button.tsx
├── AGENTS.md
└── .cursor/rules/
```

## Comandos útiles

```bash
npm run dev
npm test
```

## Notas para agentes

- Preferir **Continue/Cline + Ollama** para tareas con Rule existente
- Escalar a Cursor cloud solo si no hay patrón documentado aquí
- Responder en español salvo que el código exija inglés
