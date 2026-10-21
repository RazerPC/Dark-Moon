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
