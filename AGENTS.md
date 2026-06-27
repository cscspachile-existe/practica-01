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

## Validación sistema híbrido (2026-06-27)

| Prueba | Herramienta | Estado |
|--------|-------------|--------|
| Chat convenciones | Continue + Ollama | OK |
| Crear/editar HTML | Cline / Agent | OK |
| Button.tsx | Cline / Agent | OK |
| Rules html-practica | about.html, contact.html | OK |
| @Codebase Button | Continue `@Codebase` | Ver `src/components/Button.tsx` |
| Autocomplete | Continue 1.5B en `<footer` | Probar en `index.html` |

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
