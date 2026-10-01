# React + TypeScript + Vite

## Scripts

```bash
npm install       # install dependencies
npm run dev       # start dev server
npm run build     # type-check and build for production
npm run preview   # preview the production build
```

## Folder structure

```
@types/             # Global type declarations (*.d.ts)
public/             # Static files served as-is
src/
├── assets/         # Images, fonts, global styles
├── components/     # Presentational UI, atomic design
│   ├── atoms/      #   Smallest units (Button, Input, Label)
│   ├── molecules/  #   Small groups of atoms (SearchField, FormRow)
│   └── organisms/  #   Complex sections (Header, Footer, Form)
├── config/         # App config and constants (env values, endpoints)
├── containers/     # Stateful components: connect data/logic to components
├── hooks/          # Reusable custom hooks
├── layouts/        # Page layouts (atomic "templates")
├── libs/           # Wrappers/setup for third-party libraries
├── locales/        # Translation files
├── pages/          # Route-level screens built from layouts + containers
├── routes/         # Route definitions
├── services/       # API clients and data fetching
├── store/          # Global state
├── utils/          # Pure helper functions
├── App.tsx         # App root
├── main.tsx        # Entry point
└── vite-env.d.ts   # Vite type references
```

## Conventions

- One folder per component: `Button/Button.tsx`, `Button/Button.module.css`, `Button/index.ts`.
- Import only downward: atoms → molecules → organisms → layouts → pages.
- `components/` stay presentational (props in, UI out); data fetching and state live in `containers/`.
- `@/` maps to `src/`.
