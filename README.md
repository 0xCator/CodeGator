# CodeGator 🐊

**CodeGator** is a Java code assistant for Visual Studio Code. It formats your code to your style rules, detects code smells, refines code, and offers inline completions, all powered by a companion CodeGator server.

## Features

- **Format Java Code**: Formats Java files using your configured style (braces, indentation, naming, imports, alignment, modifier order, and more).
- **Analyze Code Smells**: Scans your Java code for code smells and can export the results as a **PDF report**.
- **Refine Java Code**: Suggests improved versions of your code.
- **Inline Completions**: Shows AI-powered code suggestions as you type in Java files.
- **Export Settings**: Saves your current CodeGator style settings to a JSON file.
- **Activity Bar View**: A dedicated CodeGator sidebar with quick access to every action.

## Commands

Open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`) and type `CodeGator`:

| Command | Description |
| --- | --- |
| `CodeGator: Format Java Code` | Format Java code using your style settings |
| `CodeGator: Analyze Java code smells` | Detect code smells and optionally export a PDF report |
| `CodeGator: Refine Java code` | Get refined versions of your code |
| `CodeGator: Export settings to JSON file` | Save your current settings to a JSON file |

## Requirements

- VS Code **1.98.0** or newer
- [Language Support for Java™ by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java) (installed automatically as a dependency)
- A running **CodeGator server**. The default address is `http://localhost:8000`.

## Extension Settings

All settings use the `javacodeassistant.` prefix.

### General

| Setting | Default | Description |
| --- | --- | --- |
| `serverUrl` | `http://localhost:8000` | URL of the CodeGator server |
| `braceStyle` | `break` | Brace style: `break` or `attach` |
| `spaceAroundOperators` | `true` | Insert spaces around operators |
| `maxLineLength` | `100` | Maximum line length |

### Modifier Order

| Setting | Description |
| --- | --- |
| `modifierOrder.class` | Order of modifiers for classes |
| `modifierOrder.method` | Order of modifiers for methods |

### Naming Conventions

Each value can be `pascalcase`, `camelcase`, `uppercase`, or a custom regex pattern.

| Setting | Default |
| --- | --- |
| `namingConventions.class` | `pascalcase` |
| `namingConventions.method` | `camelcase` |
| `namingConventions.variable` | `camelcase` |
| `namingConventions.constant` | `uppercase` |
| `namingConventions.parameter` | `camelcase` |

### Imports

| Setting | Default | Description |
| --- | --- | --- |
| `imports.order` | `preserve` | `sort` or `preserve` |
| `imports.merge` | `false` | Merge imports |

### Indentation

| Setting | Default | Description |
| --- | --- | --- |
| `indents.size` | `4` | Indent size |
| `indents.type` | `spaces` | `spaces` or `tabs` |
| `indents.switchCaseLabels` | `true` | Indent switch case labels |

### Alignments

| Setting | Default | Description |
| --- | --- | --- |
| `aligns.afterOpenBracket` | `none` | `none`, `align`, `dont_align`, `always_break`, `block_indent` |
| `aligns.parametersBeforeAlignment` | `2` | Parameters before alignment (used by `align` and `dont_align`) |

## Development

```bash
npm install
npm run compile   # or: npm run watch
```

Press `F5` in VS Code to open an Extension Development Host. Run tests with `npm test`.

## Release Notes

### 0.0.1

First release of CodeGator.
