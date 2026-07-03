# Super Calculator

## Project overview
A beginner-friendly Angular calculator app built for teaching purposes. It implements
a standard four-function calculator (add, subtract, multiply, divide) plus sign-toggle,
percent, and a light/dark theme switch. Several methods were originally left empty as
student exercises — see [Exercises](#exercises) below.

## Tech stack
- Angular 19 (standalone components, no NgModules)
- TypeScript 5.7
- Karma + Jasmine for unit tests
- RxJS 7.8, zone.js 0.15

## How to run
- Install: `npm install`
- Dev server: `npm start` → http://localhost:4200
- Tests: `npm test`
- Production build: `npm run build` (output in `dist/`)

## Project structure
```
src/
└── app/
    ├── app.component.ts      ← component logic: state (display, firstOperand,
    │                            operator, isLightMode, waitingForSecondOperand)
    │                            and button handlers (pressDigit, pressOperator,
    │                            pressEquals, pressClear, toggleTheme,
    │                            pressToggleSign, pressPercent) plus a private
    │                            calculate() helper
    ├── app.component.html    ← template: button grid, display, theme toggle
    ├── app.component.css     ← scoped styles for the calculator shell, display,
    │                            button grid, and light-mode overrides
    └── app.component.spec.ts ← unit tests (Karma + Jasmine)
```

## Exercises
This repo was built as a teaching exercise. The following were intentionally left
empty for students to implement (now completed on this branch):
- `pressToggleSign()` — flip the sign of the displayed number
- `pressPercent()` — convert the displayed number to a percentage
- `toggleTheme()` — switch between dark (default) and light mode, plus the
  corresponding light-mode CSS rules in `app.component.css`
- Several unit tests in `app.component.spec.ts` marked `🎯 YOUR TURN` (previously
  stubbed with `pending(...)`), covering display formatting, clear behavior, and
  arithmetic edge cases

See `requirements.md` for the full exercise descriptions and grading criteria.

## Coding conventions
- Button-action methods use a `press` prefix (`pressDigit`, `pressOperator`,
  `pressClear`, `pressEquals`, `pressToggleSign`, `pressPercent`)
- CSS classes follow a BEM-like convention (`btn`, `btn--operator`,
  `btn--utility`, `display__value`)
- Components are standalone (no NgModules)
- Code favors verbose, teaching-oriented comments explaining Angular concepts
  (property binding, event binding, interpolation) — keep this style when
  editing files under `src/app`
