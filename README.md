# Initialisation

`CLI`

```bash
npm create vite@latest 10-react-quiz -- --template react
npx create-vite 10-react-quiz --template react-swc
npm install -D sass
```

Either-or should work, preferably npx.
<br><b>Do not</b> use rolldown-vite during creation.
<br><b>Do not</b> install with npm and start immediately, <i>install via sass instead</i>.

`.vscode/settings.json`

```js
{
    "files.exclude": {
        ".gitignore": true,
        "eslint.config.js": true
    },
    "[javascriptreact]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    }
}
```

Afterwards:

- Wipe `App.css` and `index.css`.
- Create `index.scss`, and make sure `main.jsx` imports it.

```jsx
import "./scss/index.scss";
```

- Move `vite.svg` into `assets` (<i>optionally just clear `assets`</i>).
- Create `favicon.ico` in `public`, and update `index.html` to use it.

```html
<link rel="icon" type="image/svg+xml" href="/favicon.ico" />
```

- Create `components` folder. <b>DO NOT</b> put index.jsx or App.jsx in there.
- Remove `App.css` import from `App.jsx`.
- Replace `App.jsx`'s App() with

```jsx
export default function App() {...};
```

- Done.

# Running Instructions
First `npm i json-server -D`
Then `npm run server`
Then you may do the usual (`npx vite --port=4000`)

## React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.
Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

### React Compiler

The React Compiler is currently not compatible with SWC. See [this issue](https://github.com/vitejs/vite-plugin-react/issues/428) for tracking the progress.

### Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
