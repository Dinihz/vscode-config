# VSCode Configuration

This file documents the settings used in Visual Studio Code to optimize the development experience.

## Main Extensions

- **Vim**: Enhanced Vim experience.
- **Color Highlight**: Highlights color codes in your files.
- **ES7+ React/Redux/GraphQL/React-Native snippets**: Useful snippets for modern JavaScript.
- **Live Server**: Enables real-time web development.
- **Prettier**: Automatic code formatting.

## User Settings (`settings.json`)

```json
{
  {
  "workbench.colorTheme": "Catppuccin Mocha",
  "editor.fontSize": 14,
  "editor.fontLigatures": true,
  "editor.fontFamily": "'Hack Nerd Font Mono', 'Droid Sans Mono', 'monospace', monospace",
  "editor.lineHeight": 1.8,
  "editor.tabSize": 2,
  "editor.rulers": [80, 120],
  "workbench.startupEditor": "newUntitledFile",
  "editor.wordWrap": "on",
  "editor.minimap.renderCharacters": false,
  "telemetry.telemetryLevel": "off",
  "security.workspace.trust.untrustedFiles": "open",
  "breadcrumbs.filePath": "off",
  "outline.icons": false,
  "explorer.compactFolders": false,
  "liveServer.settings.donotShowInfoMsg": true,
  "liveServer.settings.donotVerifyTags": true,
  "editor.formatOnSave": true,
  "html.format.wrapAttributes": "auto",
  "html.format.wrapLineLength": 0,
  "html.autoClosingTags": false,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "[html]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "editor.bracketPairColorization.enabled": false,
  "symbols.hidesExplorerArrows": false,
  "symbols.files.associations": {
    "*.module.ts": "nest",
    "*.guard.ts": "typescript",
    "*.spec.ts": "ts-test",
    "*.e2e-spec.ts": "ts-test",
    "vitest.config.e2e.ts": "vite",
    ".env.example": "gear"
  },
  "files.associations": {
    "*.js": "javascriptreact"
  },
  "editor.colorDecorators": false,
  "workbench.statusBar.visible": true,
  "color-highlight.markerType": "dot-before",
  "files.autoSaveDelay": 250,
  "editor.minimap.enabled": false,
  "workbench.iconTheme": "catppuccin-mocha",
  "settingsSync.ignoredExtensions": [],
  "files.autoSave": "onFocusChange",
  "vim.easymotion": true,
  "vim.incsearch": true,
  "vim.useSystemClipboard": true,
  "vim.useCtrlKeys": true,
  "vim.hlsearch": true,
  "vim.sneak": true,
  "vim.easymotionMarkerooundColor": "#020202",
  "vim.normalModeKeyBindings": [
    {
      "before": ["<leader>", "d"],
      "after": ["d", "d"]
    },
    {
      "before": ["<tab>"],
      "commands": ["workbench.action.nextEditor"]
    },
    {
      "before": ["<S-tab>"],
      "commands": ["workbench.action.previousEditor"]
    }
  ],
  "vim.insertModeKeyBindings": [
    {
      "before": ["j", "k"],
      "after": ["<Esc>"]
    },
    {
      "before": ["<C-j>"],
      "after": ["<Esc>"]
    },
    {
      "before": ["<C-k>"],
      "after": ["<Esc>"]
    }
  ],
  "vim.visualModeKeyBindings": [
    {
      "before": [">"],
      "after": [">", "g", "v"]
    },
    {
      "before": ["<"],
      "after": ["<", "g", "v"]
    }
  ],
  "vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": ["<leader>", "d"],
      "after": ["d", "d"]
    },
    {
      "before": ["<leader>", "w"],
      "commands": ["workbench.action.splitEditor"]
    },
    {
      "before": ["<leader>", "e"],
      "commands": ["workbench.action.toggleSidebarVisibility"]
    },
    {
      "before": ["<leader>", "f"],
      "commands": ["revealInExplorer"]
    },
    {
      "before": ["<leader>", "h"],
      "after": ["_"]
    },
    {
      "before": ["<leader>", "l"],
      "after": ["$"]
    }
  ],
  "vim.leader": "<space>",

  "vim.handleKeys": {
    "<C-a>": false,
    "<C-f>": false,
    // VS Code new marker @ next occurence
    "<C-c>": false,
    // Cut
    "<C-x>": false,
    // Paste
    "<C-v>": false,
    "<C-z>": false,
    "<C-y>": false
  }
}
}
```

## Keyboard Shortcuts (`keybindings.json`)

```json
{
[
  {
    "key": "ctrl+n",
    "command": "editor.action.addSelectionToNextFindMatch",
    "when": "editorFocus"
  },
  {
    "key": "ctrl+d",
    "command": "-editor.action.addSelectionToNextFindMatch",
    "when": "editorFocus"
  },
  {
    "key": "ctrl+d",
    "command": "-list.focusPageDown",
    "when": "listFocus && !inputFocus"
  },
  {
    "key": "ctrl+;",
    "command": "workbench.action.terminal.toggleTerminal",
    "when": "terminal.active"
  },
  {
    "key": "ctrl+`",
    "command": "-workbench.action.terminal.toggleTerminal",
    "when": "terminal.active"
  },
  {
    "key": "shift+alt+k",
    "command": "editor.action.moveLinesUpAction",
    "when": "editorTextFocus && !editorReadonly"
  },
  {
    "key": "shift+alt+j",
    "command": "editor.action.moveLinesDownAction",
    "when": "editorTextFocus && !editorReadonly"
  },
  {
    "key": "tab",
    "command": "selectNextSuggestion",
    "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
  },
  {
    "key": "shift+tab",
    "command": "selectPrevSuggestion",
    "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
  },
  {
    "key": "ctrl+t",
    "command": "-extension.vim_ctrl+t",
    "when": "editorTextFocus && vim.active && vim.use<C-t> && !inDebugRepl"
  },
  {
    "key": "ctrl+t",
    "command": "-workbench.action.showAllSymbols"
  },
  {
    "key": "ctrl+k",
    "command": "-extension.vim_ctrl+k",
    "when": "editorTextFocus && vim.active && vim.use<C-k> && !inDebugRepl"
  }
]
},
```
