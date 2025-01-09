# How to Use the Quick Snippet for JavaScript Extension

This document provides step-by-step instructions on installing and using the **Multi-Language Snippet Extension** in Visual Studio Code. If you’re looking for an **overview of the available snippets** (prefixes, expansions, etc.), see the main [README.md](./README.md).

---

## 1. Prerequisites

- **Visual Studio Code** installed (version 1.80.0 or higher recommended).
- **Node.js** (only if you plan to modify and republish the extension; not required for basic usage).
- Optional: A **TypeScript** setup if you want to fully leverage TS-based snippets (interfaces, types, etc.).

---

## 2. Installation

### 2.1. From the VS Code Marketplace

1. Open **VS Code**.
2. Go to the **Extensions** panel (click the square icon in the left sidebar or press `Ctrl+Shift+X` / `Cmd+Shift+X`).
3. In the search box, type **"Quick Snippet for JavaScript"**.
4. Click **Install**.
5. Once installed, **Reload** or restart VS Code (if prompted).

### 2.2. From a VSIX File (Offline)

1. Obtain the `.vsix` file from the extension’s [Releases](#) page or another source.
2. Open **VS Code**.
3. Go to the **Extensions** panel.
4. Click the **ellipsis** (`...`) in the top-right corner → **Install from VSIX...**.
5. Select the downloaded `.vsix` file.
6. **Reload** or restart VS Code if prompted.

---

## 3. Verifying Your Installation

1. After installation, open VS Code.
2. In the **Extensions** panel, type the name of the extension in the search bar.
3. Confirm that it’s **enabled** and **up to date**.
4. If everything looks good, you’re ready to start using the snippets!

---

## 4. Basic Usage

1. **Open a file** in your desired language:
   - `.js` for JavaScript
   - `.ts` for TypeScript
   - `.jsx` / `.tsx` for React
   - `.vue` for Vue 3 Composition API
2. **Start typing** a snippet prefix (e.g., `cl`, `iface`, `rfc`, `vue-sfc`, etc.).
3. Watch as **IntelliSense** suggests the snippet in the autocomplete dropdown.
4. **Press `Tab` or `Enter`** to expand the snippet.
5. **Fill in placeholders** (like `$1`, `$2`) by typing your desired text, then press `Tab` to jump to the next placeholder.

### Example

- Open a `.js` file.
- Type `cl` and press `Tab`.
- It expands to:
  ```js
  console.log("");
  ```
