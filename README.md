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
