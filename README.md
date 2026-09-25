# dotfiles
my dotfiles

Configs live here as real files; the home-directory paths are symlinks into this repo.

| repo path                | symlinked from          |
| ------------------------ | ----------------------- |
| `.aerospace.toml`        | `~/.aerospace.toml`     |
| `.config/tmux/tmux.conf` | `~/.config/tmux/`       |
| `.config/nvim`           | `~/.config/nvim`        |

`.config/nvim` is a submodule of [Zoidt/nvim](https://github.com/Zoidt/nvim), so clone with:

```sh
git clone --recurse-submodules https://github.com/Zoidt/dotfiles.git
```

## Windows

| repo path                   | copied from                    |
| --------------------------- | ------------------------------ |
| `.glzr/glazewm/config.yaml` | `~/.glzr/glazewm/config.yaml`  |

[GlazeWM](https://github.com/glzr-io/glazewm) config. Unlike the entries above,
this is a **copy, not a symlink** — sync it manually after edits.

Requires GlazeWM **3.10.1 or newer**. Older copies of this config bound `alt+~`,
which 3.10.1's rewritten keybinding parser rejects with `Unknown key: ~`. That is
a fatal startup error, so the WM exits silently and never comes up — check
`~/.glzr/glazewm/errors.log` if that happens. The equivalent `` alt+` `` and
`` alt+shift+` `` bindings cover the same physical key.

GlazeWM cannot be upgraded via winget: it shares the package ID `glzr-io.glazewm`
with Zebar, so winget resolves to the wrong entry and refuses. Install the release
`.exe` from GitHub directly.
