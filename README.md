# Clawdmeter Card

![Clawdmeter card](images/card_preview.png)

An animated Lovelace card for the
[Clawdmeter](https://github.com/corgan2222/ha-clawdmeter) integration. It is meant to show
Claude usage (session / weekly limits, burn rate, runway, time‑to‑limit) as an animated
pixel‑art creature, mirroring the ESPHome Clawdmeter display.

The custom element is `clawdmeter-card` (use `type: custom:clawdmeter-card`).

## Status

🧪 **Early release (`v0.0.1`), experimental.** The card renders in a real Home Assistant
dashboard and ships a visual editor. It is usable, but young — expect rough edges and changes
between versions. Bug reports and ideas are welcome via the issue templates.

## Configuration

The card ships a **visual editor** — no YAML required. Open the card's edit dialog and pick your
Clawdmeter **account**; every entity is filled in automatically (matched by the integration's
translation keys, so it is language‑independent). You can also choose the **layout**
(`panel` / `hero`), set an optional **title**, and toggle each element via checkboxes, grouped as:

- **General** — title, creature, header line, background
- **Bars** — session, week, time‑to‑limit, Sonnet, Opus, extra usage
- **Values** — burn rate (5m / 30m), time to limit, limit ETA, buffer to reset, pace,
  peak today, session reset‑in

The "time‑to‑limit" bar tracks session usage toward the limit (severity‑coloured) and shows
the projected ETA, mirroring the ESPHome Clawdmeter. The card follows your Home Assistant
language (English and German included) and adapts to light/dark themes.

### YAML (optional)

```yaml
type: custom:clawdmeter-card
layout: panel # or: hero
title: Clawdmeter # optional
show: # optional per-element visibility
  background: true
  creature: true
  sonnet: false
# entity ids (session_usage, week_usage, time_to_limit, …) are filled by the editor
```

## Installation

### HACS (recommended)

1. In HACS, open the menu (⋮) → **Custom repositories**.
2. Add `https://github.com/corgan2222/lovelace-clawdmeter` with category **Dashboard**.
3. Search for **Clawdmeter Card**, install it, then reload your browser.
4. Add the card to a dashboard — the visual editor fills in your Clawdmeter account automatically.

You also need the [Clawdmeter integration](https://github.com/corgan2222/ha-clawdmeter) for the
underlying sensors.

### Manual

Copy `clawdmeter.js` to `config/www/` and add it as a dashboard resource
(`/local/clawdmeter.js`, type _JavaScript Module_), or load it via `lovelace.resources` /
`frontend.extra_module_url`.

## License

[MIT](LICENSE)
