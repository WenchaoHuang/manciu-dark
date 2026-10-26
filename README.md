# Manciu Dark

Manciu Dark is a readability-focused VS Code theme with semantic highlighting
and TextMate scope tuning for C/C++, Python, CUDA, CMake, LaTeX, Markdown,
HTML, XML, JSON/JSONC, YAML, TOML, USD ASCII (`.usda`), and Wavefront OBJ.

## Highlights

- Deep dark editor background for long coding sessions (`#1E1E1E`)
- Distinct colors for types, functions, variables, keywords, and literals
- Semantic highlighting enabled by the theme, with additional styling for
  built-ins, decorators, macros, and enum members
- Language-specific scope tuning, including blue HTML/XML tag names and
  deep red attributes, blue JSON/JSONC property names, and colors for USD
  keywords and Wavefront OBJ directives

## Color palette

| Token | Color |
| --- | --- |
| Type / Class / Enum / Namespace | Gold (`#FFD700`) |
| Function / Method | Orange (`#FF8000`) |
| Variable / Parameter / Property | Olive (`#BDB76B`) |
| Keyword / HTML tag / JSON property name | Blue (`#569CD6`) |
| Macro / Enum member / Decorator | Purple (`#BD59C5`) |
| String | Salmon (`#D69D85`) |
| Number | Light green (`#B5CEA8`) |
| Comment / Python docstring | Italic green (`#57A64A`) |
| HTML/XML attribute / Python keyword argument | Deep red (`#AA4926`) |

These are the primary colors; language-specific scopes and semantic tokens
can use more specific rules, such as blue built-in functions and classes.

## Requirements

- VS Code `^1.120.0`

Building the extension from source also requires:

- Git
- Node.js 20 or later
- npm

## Recommended language extensions

Manciu Dark provides the color theme, while language extensions provide the
syntax and semantic information needed for accurate highlighting. Install the
matching VS Code extension for the files you use:

| File type | VS Code extension |
| --- | --- |
| `.usda` | USD Language |
| `.toml` | Even Better TOML |
| `CMakeLists.txt`, `.cmake` | CMake Tools |
| `.tex`, `.sty`, `.cls` | LaTeX language support |
| `.md` | MyST-Markdown |
| `.py`, `.pyi` | Pylance |

VS Code includes syntax highlighting for HTML, XML, JSON/JSONC, and Markdown.
The final colors depend on the scopes and semantic tokens supplied by the
active language extension.

## Installation

### VS Code Marketplace

Install Manciu Dark from the
[Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=Manciu.manciu-dark),
or search for **Manciu Dark** in the VS Code Extensions view.

You can also install it from the command line:

```bash
code --install-extension Manciu.manciu-dark
```

### Build from source

To build a VSIX package locally, clone the repository and run `vsce`:

```bash
git clone https://github.com/WenchaoHuang/manciu-dark.git
cd manciu-dark
npx --yes @vscode/vsce@3.9.2 package
```

The command creates `manciu-dark-0.2.0.vsix` in the repository root. Install it
from the command line:

```bash
code --install-extension ./manciu-dark-0.2.0.vsix
```

Alternatively, open the Extensions view in VS Code, select the `...` menu,
choose **Install from VSIX...**, and select the generated file.

## Usage

After installation:

1. Open the Command Palette with `Ctrl+Shift+P` on Windows/Linux or
   `Cmd+Shift+P` on macOS.
2. Run **Preferences: Color Theme**.
3. Select **Manciu Dark**.

You can also select the theme in `settings.json`:

```json
{
  "workbench.colorTheme": "Manciu Dark",
  "editor.semanticHighlighting.enabled": "configuredByTheme"
}
```

The theme enables semantic highlighting by default. If colors appear different
from those described above, check that semantic highlighting is enabled, the
appropriate language extension is active, and your token color customizations
are not overriding the theme.

## Development

The theme definition is located at
[`themes/Manciu Dark-color-theme.json`](themes/Manciu%20Dark-color-theme.json).
It uses JSON with comments (JSONC), including trailing commas.

1. Clone and open the repository in VS Code.
2. Press `F5` to launch an Extension Development Host.
3. Select **Manciu Dark** in the new window.
4. Use **Developer: Inspect Editor Tokens and Scopes** to inspect syntax scopes
   when adjusting token colors.

Inspect the package contents and create a local VSIX with:

```bash
npx --yes @vscode/vsce@3.9.2 ls --tree
npx --yes @vscode/vsce@3.9.2 package
```

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for version history.

## Feedback

Report problems and scope suggestions through [GitHub Issues].

## License

Manciu Dark is available under the [MIT License](LICENSE).

[GitHub Issues]: https://github.com/WenchaoHuang/manciu-dark/issues
