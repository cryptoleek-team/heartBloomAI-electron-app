## Elect Avatar

A minimal Electron wrapper that opens a window and loads a local web app at `http://localhost:5173/auto-init`.

## Prerequisites

- Node.js 18+ and npm
- A web app/dev server running at `http://localhost:5173/auto-init` (e.g., Vite)

## Install

```bash
npm install
```

## Run (development)

In one terminal, start your web app so it serves `http://localhost:5173/auto-init`.

In another terminal, start Electron:

```bash
npm start
```

## Configure the URL

The Electron window loads a URL defined in `index.js`:

```js
win.loadURL('http://localhost:5173/auto-init');
```

Change this to point to your app (local dev server or a built `file://` URL) as needed.

## Project Scripts

- `npm start`: Launches Electron using the entry `index.js`.

## Notes

- The window is frameless (`frame: false`) and uses a hidden title bar (`titleBarStyle: 'hidden'`). Ensure your web app provides its own draggable region and window controls if needed.
- `nodeIntegration` is enabled and `contextIsolation` is disabled for simplicity. For production, consider hardening these settings.

## License

ISC
