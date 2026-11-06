# Ghostty configuration

A personal Ghostty configuration for Ubuntu 26.04, with the **12-bit Rainbow** theme, a translucent terminal background, and a compact title bar and tab bar.

## Files

| File | Purpose |
| --- | --- |
| [`ubuntu-26.04/config.ghostty`](ubuntu-26.04/config.ghostty) | Terminal appearance, font, cursor, window, and tab settings. |
| [`ubuntu-26.04/titlebar-transparency.css`](ubuntu-26.04/titlebar-transparency.css) | GTK styling for the title bar and tab bar. |

## Installation

Install [Ghostty](https://ghostty.org/docs/install) first. From the root of this repository, copy the files into your Ghostty configuration directory:

```sh
mkdir -p ~/.config/ghostty
cp -i ubuntu-26.04/config.ghostty ~/.config/ghostty/config.ghostty
cp -i ubuntu-26.04/titlebar-transparency.css ~/.config/ghostty/titlebar-transparency.css
```

The `-i` option asks before replacing an existing file. Back up or merge any existing settings you want to keep. Ghostty may also load `~/.config/ghostty/config`, whose conflicting settings take precedence over `config.ghostty`.

These paths assume the default Linux configuration directory. If you set `XDG_CONFIG_HOME`, see the [Ghostty configuration documentation](https://ghostty.org/docs/config) for its configuration path; the `gtk-custom-css` path in this repository's config still points to `~/.config/ghostty/titlebar-transparency.css`.

Restart Ghostty, or press **Ctrl+Shift+,** to reload the configuration. Some changes may require a restart.

## Appearance

- The terminal background is set to 80% opacity, with a blur radius of 25.
- The title bar and tab bar share a compact layout and a translucent dark background.
- The font size is 9; window padding is 12 pixels horizontally and vertically.

Transparency and blur depend on your desktop environment and compositor. On Linux, Ghostty's documented blur support is limited to certain environments; other desktops may require additional configuration or extensions. See the [configuration reference](https://ghostty.org/docs/config/reference) for details.

To customize the setup, edit the installed configuration and CSS files, then reload or restart Ghostty.
