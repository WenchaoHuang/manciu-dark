# Manciu Dark

Manciu Dark is a readability-focused VS Code theme with semantic highlighting
and TextMate scope tuning for C/C++, Python, CMake, CUDA, LaTeX, and common data
formats.

## Highlights

- Deep dark editor background for long coding sessions (`#1E1E1E`)
- Strong semantic color separation for faster code scanning:
  - Type / Class / Enum: Gold (`#FFD700`)
  - Function / Method: Orange (`#FF8000`)
  - Variable / Parameter: Olive (`#BDB76B`)
  - Keyword: Blue (`#569CD6`)
  - Comment: Italic Green (`#57A64A`)
- Semantic highlighting enabled
- Additional scope tuning for C++, Python, CUDA, CMake, JSON, YAML, TOML, XML,
  and LaTeX

## Requirements

- VS Code `^1.120.0`

Building the extension from source also requires:

- Git
- Node.js 20 or later
- npm

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

This repository does not provide GitHub Release packages or prebuilt `.vsix`
files. To package the extension locally, clone the repository and run `vsce`:

```bash
git clone https://github.com/WenchaoHuang/manciu-dark.git
cd manciu-dark
npx --yes @vscode/vsce@3.9.2 package
```

The command creates `manciu-dark-0.1.0.vsix` in the repository root. Install it
from the command line:

```bash
code --install-extension ./manciu-dark-0.1.0.vsix
```

Alternatively, open the Extensions view in VS Code, select the `...` menu,
choose **Install from VSIX...**, and select the generated file.

## Usage

After installation:

1. Open the Command Palette with `Ctrl+Shift+P` on Windows/Linux or
   `Cmd+Shift+P` on macOS.
2. Run **Preferences: Color Theme**.
3. Select **Manciu Dark**.

## Development

The theme definition is located at `themes/Manciu Dark-color-theme.json`.

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
