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

- Páginas con CSS inline, fondo `#1a1a2e`, copy en español
- Ver `.cursor/rules/html-practica.mdc` e `index.html`

### Componentes UI

- `Button` con variantes `primary` / `secondary` en `src/components/Button.tsx`
- Ver `.cursor/rules/button-component.mdc`

### Autenticación

- (pendiente — escalar a cloud si se implementa JWT)

### API

- (pendiente — REST + Zod cuando aplique)

## Estructura del repo

```
/
├── index.html
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
