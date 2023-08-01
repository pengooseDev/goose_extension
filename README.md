# Goose Extension Boilerplate

This is a Google Chrome extension boilerplate in a ReactJS + Typescript + Vite environment. Initial project configurations and required manifest and rollupOptions for bundling are all set.

## Quick Start

Clone the repository:

```bash
git clone https://github.com/pengooseDev/goose_extension.git
```

## Using the Boilerplate

A Chrome extension consists of the following components:

1. background
2. options
3. popup

You can modify and expand these files depending on the functionality you want to implement.

The project uses Vite to bundle the extension. Rollup settings in vite.config.ts are set by default and can be changed as needed.

```arduino
src
├─ background
│ ├─ background.html
│ └─ background.ts
├─ options
│ ├─ App.tsx
│ ├─ options.html
│ └─ options.tsx
├─ popup
│ ├─ App.tsx
│ ├─ popup.html
│ ├─ popup.tsx
│ └─ assets
│   └─ logo.ico
└─ manifest.json
```

## Production Build

Once you have implemented the functionality, you need to build it into a static file.

```bash
npm run build
```

After running npm run build, the dist directory will contain the production-ready extension. Load the static files into Chrome as follows:

- Go to [this page](chrome://extensions) to open the extension management page.
- Click on the Chrome menu, hover over "More Tools", and select "Extensions" to open this page.
- Click on the toggle switch next to "Developer mode" to enable Developer mode.
- Click on the "Load unpacked" button and upload the dist directory.

Your extension is now loaded and ready for use! 😉

# Contribution

Contributions to this boilerplate are welcome! If you want to suggest changes or improvements, please submit a pull request or open an issue. 😆
