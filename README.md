# Dark Moon Theme

A minimal dark theme for Home Assistant: graphite cards, cool silver accents and a soft silver glow on hover.

> **For the full look, install [card-mod](https://github.com/thomasloven/lovelace-card-mod).**
> Without it the theme still works (dark colors, borders, shadows, readable inputs), but cards are flat and there is no gradient or hover glow.

![Dark Moon](images/preview.png)

## Features

- Near-black background with graphite cards
- Subtle top-to-bottom gradient on cards *(card-mod)*
- Silver border and glow on hover, mouse only, never stuck on touch screens *(card-mod)*
- Thin neutral borders and a tight shadow that never spills onto neighbouring cards
- Readable text fields, dropdowns, dialogs, switches and sliders
- Works great with [Mushroom](https://github.com/piitaya/lovelace-mushroom) cards
- Does not change font sizes, icon sizes, spacing or your cards' icon colors

## Installation

### HACS (recommended)

[![Open your Home Assistant instance and open a repository inside HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=RazerPC&repository=Dark-Moon&category=theme)

1. Open HACS and search for **Dark Moon Theme**, or click the button above.
2. Download it.
3. Use **Quick reload** (Settings → System → Restart Home Assistant) to load the theme.

### Manual

1. Copy `themes/dark_moon.yaml` into your `config/themes/` folder.
2. Use **Quick reload** (Settings → System → Restart Home Assistant) to load the theme.

In both cases, `configuration.yaml` must load themes:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

## Usage

1. Open your **Profile**.
2. Under **Theme**, choose **Dark Moon**.
3. Set the mode to **Dark**.

Dark Moon only has a dark variant. If the mode is set to Auto and your device is in light mode, Home Assistant mixes in its own light colors and some text becomes hard to read.

## License

MIT
