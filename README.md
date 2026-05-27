# Manciu Dark

Manciu Dark is a VS Code dark theme focused on code readability, with semantic highlighting tuned for C/C++, Python, and CMake workflows.

## Highlights

- Deep dark editor background for long coding sessions (#1E1E1E)
- Strong semantic color separation for faster code scanning:
	- Type / Class / Enum: Gold (#FFD700)
	- Function / Method: Orange (#FF8000)
	- Variable / Parameter: Olive (#BDB76B)
	- Keyword: Blue (#569CD6)
	- Comment: Italic Green (#57A64A)
- Semantic highlighting enabled
- Additional scope tuning for C++, Python, CUDA, and CMake

## Requirements

- VS Code ^1.120.0

## Installation

### Option 1: Install local VSIX (recommended)

This repository already includes a packaged extension file:

- manciu-dark-0.0.1.vsix

You can install it with either method below:

1. Open Extensions in VS Code.
2. Click the ... menu in the top-right corner.
3. Select Install from VSIX....
4. Choose manciu-dark-0.0.1.vsix.

Or use the command line:

```bash
code --install-extension manciu-dark-0.0.1.vsix
```

### Option 2: Run in extension development mode

1. Open this project folder in VS Code.
2. Press F5 to launch an Extension Development Host.
3. In the new window, run Preferences: Color Theme.
4. Select Manciu Dark.

## Usage

After installation:

1. Open the Command Palette (Ctrl+Shift+P).
2. Run Preferences: Color Theme.
3. Select Manciu Dark.

## Development

Theme definition file:

- themes/Manciu Dark-color-theme.json

Repackage after changes:

```bash
npx @vscode/vsce package
```

A new .vsix file will be generated for local installation and testing.

## Changelog

See CHANGELOG.md for version history.
