# Quick Snippet for JavaScript Extension

A convenient Visual Studio Code extension providing a curated set of **snippets** for:

- **JavaScript** (ES6+)
- **TypeScript**
- **React** (JS/TS)
- **Vue 3 (Composition API)**

This extension aims to help developers quickly scaffold boilerplate code in a consistent, idiomatic way.

---

## Features

1. **JavaScript Snippets**  
   Common patterns like for loops, arrow functions, console logging, and fetch requests.

2. **TypeScript Snippets**  
   Interfaces, type aliases, enums, classes, and typed async functions.

3. **React Snippets**  
   Functional components (JS/TS), hooks (`useState`, `useEffect`), context creation, React Router boilerplate.

4. **Vue Snippets (Composition API)**  
   Focused on Vue 3 with `<script setup>`, reactivity (`ref`, `computed`), lifecycle hooks, typed props/emits, etc.

---

## Installation

1. **From VS Code Marketplace (Recommended)**

   - Open **Extensions** in VS Code (Ctrl+Shift+X or Cmd+Shift+X).
   - Search for "**Quick Snippet for JavaScript**".
   - Click **Install**.
     OR goto [Marketplace](https://marketplace.visualstudio.com/items?itemName=YAKAZAKI.quick-snip-js) to install

2. **From `.vsix` file (Offline)**
   - Download the `.vsix` file (from [Releases](#) or a direct link).
   - In VS Code, go to **Extensions** → **...** → **Install from VSIX**.
   - Select the downloaded file.

---

## Usage

1. **Open a file** in your language of choice:

   - JavaScript (`.js`)
   - TypeScript (`.ts`)
   - React (`.jsx` / `.tsx`)
   - Vue (`.vue`)

2. **Type one of the snippet prefixes** (e.g. `cl`, `iface`, `rfc`, `vue-sfc`, etc.).
3. **Press `Tab`** (or `Enter`) to expand the snippet.
4. **Tab through placeholders** to quickly fill in variable names, function parameters, or other details.

---

## Snippet Reference

Below are some of the most frequently used prefixes for each language/framework, along with a brief description and the resulting expansion.

### JavaScript

| **Prefix** | **Description**                       | **Expansion (simplified)**                                                                                                              |
| ---------- | ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `cl`       | Insert `console.log()`                | `js\nconsole.log('');\n`                                                                                                                |
| `clm`      | Log multiple variables                | `js\nconsole.log('var1:', var1, 'var2:', var2);\n`                                                                                      |
| `afn`      | Arrow function                        | `js\nconst fnName = (params) => {\n  // ...\n}\n`                                                                                       |
| `afna`     | Async arrow function (with try/catch) | `js\nconst fnName = async (params) => {\n  try {\n    // ...\n  } catch (err) {\n    console.error(err);\n  }\n}\n`                     |
| `forloop`  | Classic for loop                      | `js\nfor (let i = 0; i < array.length; i++) {\n  const item = array[i];\n  // ...\n}\n`                                                 |
| `forof`    | For...of loop                         | `js\nfor (const item of items) {\n  // ...\n}\n`                                                                                        |
| `iife`     | Immediately Invoked Function          | `js\n(function() {\n  // ...\n})();\n`                                                                                                  |
| `fetchget` | Basic fetch GET request               | `js\nfetch('URL')\n  .then(res => res.json())\n  .then(data => {\n    console.log(data);\n  })\n  .catch(err => console.error(err));\n` |
| `tryc`     | Try/catch block                       | `js\ntry {\n  // ...\n} catch (error) {\n  console.error(error);\n}\n`                                                                  |
| `sto`      | setTimeout boilerplate                | `js\nsetTimeout(() => {\n  // ...\n}, 1000);\n`                                                                                         |

---

### TypeScript

| **Prefix** | **Description**                   | **Expansion (simplified)**                                                                                                                                 |
| ---------- | --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `clt`      | Console log (TS)                  | `ts\nconsole.log('');\n`                                                                                                                                   |
| `iface`    | Interface declaration             | `ts\ninterface MyInterface {\n  // ...\n}\n`                                                                                                               |
| `talias`   | Type alias                        | `ts\ntype MyType = {\n  // ...\n};\n`                                                                                                                      |
| `tenum`    | Enum declaration                  | `ts\nenum MyEnum {\n  VALUE1 = 'VALUE1',\n  VALUE2 = 'VALUE2'\n}\n`                                                                                        |
| `tclass`   | Class with constructor            | `ts\nclass MyClass {\n  constructor(params) {\n    // ...\n  }\n}\n`                                                                                       |
| `tfunc`    | Function with typed params/return | `ts\nfunction myFunc(param: Type): ReturnType {\n  // ...\n}\n`                                                                                            |
| `tasync`   | Async function with return type   | `ts\nasync function myFunc(param: Type): Promise<ReturnType> {\n  try {\n    // ...\n  } catch (err) {\n    console.error(err);\n    throw err;\n  }\n}\n` |
| `tgen`     | Generic function                  | `ts\nfunction myFunc<T>(arg: T): T {\n  // ...\n  return arg;\n}\n`                                                                                        |
| `troarr`   | Readonly array                    | `ts\nconst arr: ReadonlyArray<Type> = [];\n`                                                                                                               |
| `tpartial` | TypeScript Partial utility type   | `ts\ntype PartialMyInterface = Partial<MyInterface>;\n`                                                                                                    |

---

### React (JS/TS)

| **Prefix**   | **Description**                                | **Expansion (simplified)**                                                                                                                                                                                                                                                                                          |
| ------------ | ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `rfc`        | React functional component (JS)                | `jsx\nimport React from 'react';\n\nconst MyComponent = () => {\n  return <div></div>;\n};\nexport default MyComponent;\n`                                                                                                                                                                                          |
| `rfc-ts`     | React functional component (TS with interface) | `tsx\nimport React from 'react';\n\ninterface Props {\n  // define props\n}\n\nconst MyComponent: React.FC<Props> = () => {\n  return <div></div>;\n};\nexport default MyComponent;\n`                                                                                                                              |
| `usest`      | useState hook                                  | `jsx\nconst [state, setState] = React.useState(initialValue);\n`                                                                                                                                                                                                                                                    |
| `useeff`     | useEffect hook                                 | `jsx\nReact.useEffect(() => {\n  // ...\n}, [dependency]);\n`                                                                                                                                                                                                                                                       |
| `usectx`     | useContext hook                                | `jsx\nconst value = React.useContext(MyContext);\n`                                                                                                                                                                                                                                                                 |
| `ctx-create` | Create a React context + provider              | `ts\nconst MyContext = React.createContext<MyType>(defaultValue);\n\nexport function MyProvider({ children }: { children: React.ReactNode }) {\n  return (\n    <MyContext.Provider value={/* ... */}>\n      {children}\n    </MyContext.Provider>\n  );\n}\n\nexport default MyContext;\n`                        |
| `rroute`     | Basic React Router (v6) setup                  | `jsx\nimport { BrowserRouter as Router, Routes, Route } from 'react-router-dom';\n\nfunction App() {\n  return (\n    <Router>\n      <Routes>\n        <Route path='/' element={<Home />} />\n        <Route path='/about' element={<About />} />\n      </Routes>\n    </Router>\n  );\n}\nexport default App;\n` |
| `rchook`     | Custom React hook boilerplate                  | `jsx\nimport React from 'react';\n\nexport function useCustomHook() {\n  const [state, setState] = React.useState(null);\n  React.useEffect(() => {\n    // side effect\n  }, []);\n  return { state, setState };\n}\n`                                                                                             |
| `rmemo`      | Memoized React component                       | `jsx\nimport React from 'react';\n\nconst MyComponent = React.memo(() => {\n  return <div></div>;\n});\n\nexport default MyComponent;\n`                                                                                                                                                                            |
| `usered`     | useReducer hook                                | `jsx\nconst [state, dispatch] = React.useReducer((s, action) => {\n  switch (action.type) {\n    case 'TYPE':\n      return { ...s, /* ... */ };\n    default:\n      return s;\n  }\n}, {});\n`                                                                                                                    |

---

### Vue (Composition API, `<script setup>`)

| **Prefix**      | **Description**                                      | **Expansion (simplified)**                                                                                                                           |
| --------------- | ---------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| `vue-sfc`       | Basic Vue 3 SFC using `<script setup>`               | `html\n<template>\n  <div></div>\n</template>\n\n<script setup lang=\"ts\">\n// import { ref } from 'vue';\n</script>\n\n<style scoped>\n</style>\n` |
| `vdefineprops`  | Define typed props                                   | `ts\ninterface Props {\n  propA: string;\n}\n\nconst props = defineProps<Props>();\n`                                                                |
| `vdefineemits`  | Define typed emits                                   | ```ts\ninterface Emits {\n (event: 'custom-event', payload: string                                                                                   | number): void;\n}\n\nconst emit = defineEmits<Emits>();\n``` |
| `vdefineexpose` | Expose component internals (e.g., methods) to parent | `ts\ndefineExpose({\n  methodName,\n});\n`                                                                                                           |
| `vref`          | Create a reactive ref                                | `ts\nimport { ref } from 'vue';\n\nconst variable = ref(null);\n`                                                                                    |
| `vcomputed`     | Create a computed property                           | `ts\nimport { computed } from 'vue';\n\nconst myComputed = computed(() => {\n  // ...\n});\n`                                                        |
| `vwatch`        | Watch a reactive source                              | `ts\nimport { watch } from 'vue';\n\nwatch(() => source, (newVal, oldVal) => {\n  // ...\n});\n`                                                     |
| `vwatcheffect`  | WatchEffect to auto-track dependencies               | `ts\nimport { watchEffect } from 'vue';\n\nwatchEffect(() => {\n  // ...\n});\n`                                                                     |
| `vonmounted`    | Lifecycle: onMounted                                 | `ts\nimport { onMounted } from 'vue';\n\nonMounted(() => {\n  // ...\n});\n`                                                                         |
| `vonunmounted`  | Lifecycle: onUnmounted                               | `ts\nimport { onUnmounted } from 'vue';\n\nonUnmounted(() => {\n  // ...\n});\n`                                                                     |

> **Note**: Remove `lang="ts"` or the TypeScript interfaces if you aren’t using TypeScript with Vue.

---

## Customizing Snippets

1. **Prefixes**: Change the snippet prefixes if you prefer different abbreviations.
2. **Placeholders**: Add more placeholders (`$1`, `$2`, etc.) or choice fields (`"${1|log,warn,error|}"`).
3. **Remove Type Annotations**: If you’re not using TS, remove `lang="ts"` and any interfaces or generics.

---

## Contributing

1. **Fork** the ([Repository](https://github.com/nepalibidur14/vs-quicksnippet)).
2. **Add or edit snippets** in their respective JSON files.
3. **Submit a pull request** with your changes.

We welcome snippets for additional frameworks, advanced language features, or any repetitive patterns!

---

## License

Licensed under the [MIT License](LICENSE.md). Feel free to reuse or modify this extension in your own projects.

---

## Feedback & Support

- **Bugs or feature requests?**  
  [Open an issue](https://github.com/nepalibidur14/vs-quicksnippet/issues).
- **Enjoying it?**  
  Please leave a [rating or review](https://marketplace.visualstudio.com/items?itemName=YAKAZAKI.quick-snip-js&ssr=false#review-details) in the VS Code Marketplace!

---

### Happy Coding with JavaScript, TypeScript, React, and Vue 3 Composition API!
