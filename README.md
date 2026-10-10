# Dark Moon

A minimal dark theme for Home Assistant: graphite cards, cool silver accents and a soft silver glow on hover.

![Dark Moon](images/preview.png)

## Features

- Near-black background with graphite cards and a subtle top-to-bottom gradient
- Thin neutral borders and a tight shadow that never spills onto neighbouring cards
- Silver border and glow on hover (mouse only, never stuck on touch screens)
- Readable text fields, dropdowns, dialogs, switches and sliders
- Works great with [Mushroom](https://github.com/piitaya/lovelace-mushroom) cards
- Does not change font sizes, icon sizes, spacing or your cards' icon colors

## Requirements

- [card-mod](https://github.com/thomasloven/lovelace-card-mod) is **recommended**, not required.
  - With card-mod: graphite gradient on cards and silver hover effect.
  - Without card-mod: everything else works; cards are a flat `#17181b` and there is no hover effect.

## Installation

### HACS

[![Open your Home Assistant instance and open a repository inside HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=RazerPC&repository=Dark-Moon&category=theme)

1. Open HACS and search for **Dark Moon**, or add this repository as a custom repository (type: Theme).
2. Download it.
3. Use **Quick reload** (Settings → System → Restart Home Assistant) to load the theme.

### Manual

1. Copy `themes/dark_moon.yaml` into your `config/themes/` folder.
2. Use **Quick reload** (Settings → System → Restart Home Assistant) to load the theme.

Either way, `configuration.yaml` must load themes:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

## Usage

1. Open your **Profile**.
2. Under **Theme**, choose **Dark Moon**.
3. Set the mode to **Dark**.

Dark Moon only has a dark variant. If the mode is set to Auto and your device is in light mode, Home Assistant mixes in its own light colors and some text becomes hard to read.

## Per-card customization (card-mod)

Use your own background color on a single card:

```yaml
card_mod:
  style: |
    ha-card {
      --dark-moon-card-gradient: none;
      --ha-card-background: #2b1d0e;
    }
```

Or replace the gradient with your own:

```yaml
card_mod:
  style: |
    ha-card {
      --dark-moon-card-gradient: linear-gradient(180deg, #24324a 0%, #182235 100%);
    }
```

## Theme customization

| What | Where | Default |
| --- | --- | --- |
| Card gradient | `linear-gradient(...)` in `card-mod-card` | `#1a1b1f` → `#141518` |
| Hover border | `border-color` in `card-mod-card` | `rgba(226, 232, 240, 0.50)` |
| Hover glow | `0 0 10px rgba(226, 232, 240, 0.24)` | 10px, 24% |
| Resting border | `ha-card-border-color` | `rgba(255, 255, 255, 0.06)` |
| Card corner radius | `ha-card-border-radius` | `16px` |
| Accent color | `primary-color`, `accent-color` | `#c9d1d9` |
| Page background | `primary-background-color` | `#0b0c0e` |

## License

MIT
