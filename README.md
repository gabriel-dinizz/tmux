# tmux config

Config location: `~/.config/tmux/tmux.conf`

## Prefix

`Ctrl+a` (instead of default `Ctrl+b`)

## Key Bindings

### Panes
| Key | Action |
|-----|--------|
| `prefix + \|` | Split horizontally |
| `prefix + -` | Split vertically |
| `prefix + h/j/k/l` | Navigate panes (Vim-style) |
| `prefix + H/J/K/L` | Resize panes by 5 |

### Windows
| Key | Action |
|-----|--------|
| `prefix + c` | New window (keeps current path) |

### Copy Mode (Vi-style)
| Key | Action |
|-----|--------|
| `prefix + Enter` | Enter copy mode |
| `v` | Begin selection |
| `y` | Copy selection and exit |

### General
| Key | Action |
|-----|--------|
| `prefix + r` | Reload config |

## Settings

- Mouse support enabled
- Scrollback buffer: 10,000 lines
- Windows/panes start at index 1
- Escape time: 10ms (Neovim-friendly)
- Focus events enabled (Neovim autoread)
- True color support

## Troubleshooting

If tmux fails with `open terminal failed: not a terminal`, remove the stale socket:

```sh
rm /tmp/tmux-$(id -u)/default
tmux
```
