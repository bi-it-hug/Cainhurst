# Miasma

A quiet, near-black dark theme for Visual Studio Code.

Miasma uses a neutral grey scale with no tint at all: no blue cast and no warm cast. It adds muted status colors and the familiar Dark+ syntax highlighting. The sidebars, editor and panel sit like cards on a near-black shell, in the style of [shadcn/ui](https://ui.shadcn.com).

> _Miasma_: the "bad air" once blamed for the plague. Dark, quiet, and everywhere.

## Features

- **Neutral greys.** The whole UI uses the Tailwind neutral scale, from `#0a0a0a` to `#fafafa`, so the chrome never tints your code.
- **Card layout.** The editor, sidebars and panel are `#171717` surfaces with a faint 10% white border, set on a `#0a0a0a` shell.
- **Muted accents.** Errors, warnings, Git changes and diffs use Tailwind hues with their saturation reduced, so they don't look neon next to the greys.
- **Familiar syntax.** Token colors follow VS Code's Dark+, so your code looks the way you're used to.
- **Near-complete coverage.** The theme sets 969 of VS Code's 971 workbench colors on purpose, including newer areas such as the Chat and agent views.

## Installation

1. Open the **Extensions** view (`Ctrl+Shift+X`, or `Cmd+Shift+X` on macOS).
2. Search for **Miasma** and click **Install**.
3. Open the Command Palette (`Ctrl+Shift+P`), run **Preferences: Color Theme** and choose **Miasma**.

You can also install it from Quick Open (`Ctrl+P`):

```
ext install bi-it-hug.miasma
```

## Palette

| Role                     | Color     |
| ------------------------ | --------- |
| Shell (title/status bar) | `#0a0a0a` |
| Surfaces                 | `#171717` |
| Raised, active           | `#262626` |
| Selection, hover         | `#404040` |
| Dimmed text              | `#737373` |
| Muted text               | `#a1a1a1` |
| Text                     | `#e5e5e5` |
| Bright text, icons       | `#fafafa` |
| Error, deleted           | `#e57c79` |
| Warning                  | `#f2be5b` |
| Info, modified           | `#63a3ee` |
| Success, added           | `#6abd77` |

## Development

Clone the repository, open it in VS Code and press `F5`. This launches an Extension Development Host with the theme loaded.

- **Workbench colors** are generated. Edit `scripts/build-theme.mjs`, not the `colors` object in the JSON, and then run:

  ```sh
  node scripts/build-theme.mjs          # rewrite "colors" in themes/miasma-color-theme.json
  node scripts/build-theme.mjs --check  # report coverage only, write nothing
  ```

- **Syntax colors** (`tokenColors`) are edited by hand in `themes/miasma-color-theme.json`.

Issues and pull requests are welcome at [github.com/bi-it-hug/miasma](https://github.com/bi-it-hug/miasma/issues).

## License

[MIT](LICENSE.txt)
