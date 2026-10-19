# VS Code Dark 2026 for Fresh

`vscode-dark-2026.json` ports the saved active Dark 2026 palette from the
locally installed VS Code 1.140.0. It extends Fresh's built-in `dark` theme.

Install the JSON file under `~/.config/fresh/themes/`, then select
`vscode-dark-2026` with **Select Theme**, or set `"theme": "vscode-dark-2026.json"`
in Fresh's user configuration. Restart Fresh to load newly installed themes.

The port covers editor colors, tabs, menus, popups, status indicators, search,
diagnostics, scrollbars, the terminal, and Git file status. VS Code's translucent
colors are composited onto the corresponding background and stored as solid RGB.
Bracket and indentation rainbows use the standard VS Code dark bracket palette.
Fresh-only colors without a counterpart inherit from `dark`.

Syntax colors are approximations within Fresh's existing categories. Keywords
use Dark 2026's general keyword color; control-flow keywords cannot be colored
separately. Numbers and constants share Fresh's `constant` color, so the port
uses VS Code's numeric color. Properties share the variable color; attributes
share the constant color. TextMate scope-specific rules and semantic token
overrides are not preserved by a Fresh theme file.

Validation: checked all 135 RGB entries and their keys against Fresh's theme
schema, and confirmed that the installed Fresh 0.5.3 renders the configured
editor, tab, menu, and syntax colors in a truecolor terminal.
