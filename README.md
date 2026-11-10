<p align="center">
  <img src="https://raw.githubusercontent.com/corgan2222/lovelace-clawdmeter/main/images/header.png" alt="Clawdmeter Card" width="840">
</p>

<h1 align="center">Clawdmeter Card — Animated Claude Usage for Home Assistant</h1>

<p align="center"><em>Your Claude usage as a living pixel-art creature on the dashboard.</em></p>

<p align="center">
  <a href="https://www.home-assistant.io/integrations/marketplace/"><img alt="Marketplace Custom" src="https://img.shields.io/badge/Marketplace-Custom-41BDF5.svg"></a>
  <img alt="Lovelace" src="https://img.shields.io/badge/Lovelace-card-1c8edb.svg">
  <img alt="i18n" src="https://img.shields.io/badge/i18n-EN%20%2F%20DE-success.svg">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-green.svg">
</p>

<p align="center">
  <a href="https://my.home-assistant.io/redirect/hacs_repository/?owner=corgan2222&repository=lovelace-clawdmeter&category=plugin"><img alt="Open the repository in Home Assistant" src="https://my.home-assistant.io/badges/hacs_repository.svg"></a>
</p>

<p align="center">
  <a href="https://github.com/corgan2222/esphome-modular-lvgl-buttons"><img src="https://raw.githubusercontent.com/corgan2222/lovelace-clawdmeter/main/images/clawdmeter-esp-display.png" alt="Clawdmeter ESPHome display" height="40"></a>
  <a href="https://github.com/corgan2222/ha-clawdmeter"><img src="https://raw.githubusercontent.com/corgan2222/lovelace-clawdmeter/main/images/clawdmeter-ha-integration.png" alt="Clawdmeter Home Assistant integration" height="40"></a>
  <a href="https://github.com/corgan2222/lovelace-clawdmeter"><img src="https://raw.githubusercontent.com/corgan2222/lovelace-clawdmeter/main/images/clawdmeter-lovelace-card.png" alt="Clawdmeter Lovelace card" height="40"></a>
</p>

An animated Lovelace card for the
[Clawdmeter](https://github.com/corgan2222/ha-clawdmeter) integration. It is meant to show
Claude usage (session / weekly limits, burn rate, runway, time‑to‑limit) as an animated
pixel‑art creature, mirroring the ESPHome Clawdmeter display.

The custom element is `clawdmeter-card` (use `type: custom:clawdmeter-card`).

## ✨ Highlights

- **Animated pixel-art creature** — its mood (idle → heavy) follows your burn rate, and the frame glows green/orange/red with the runway pace.
- **Two layouts** — `panel` and `hero`, switchable in the visual editor.
- **Visual editor, no YAML** — pick your Clawdmeter account and every entity is filled in automatically (matched by the integration's translation keys, so it is language-independent).
- **Session, weekly, Sonnet & Opus bars** plus burn rate, time-to-limit, ETA, pace and peak values.
- **Per-model weekly cap** (for example Fable) with its reset, extra usage with the amount spent, and the week split by surface (Claude Code, chat, Cowork).
- **Graph inside the card** — the built-in history or statistics graph, or Mini Graph Card and ApexCharts Card when installed. With ApexCharts the graph shows reset lines, a look ahead and the trend to the limit.
- **Plans without a session limit** (Ultra) — the card follows the weekly window instead of showing the same numbers twice.
- **Theme-aware** — adapts to light/dark themes; turn the background off to blend into your own theme.
- **English & German**, following your Home Assistant language.

<p align="center">
  <img src="https://raw.githubusercontent.com/corgan2222/lovelace-clawdmeter/main/images/card_preview.png" alt="Clawdmeter card" width="840">
</p>

## Status

🧪 **Beta (`v0.1.0`).** The card renders in a real Home Assistant dashboard and ships a
visual editor. It is usable day-to-day, but still maturing — expect the odd rough edge and
some changes between versions. Bug reports and ideas are welcome via the issue templates.

## Screenshots

Taken on a plan without a session limit (Ultra), so the card follows the weekly window.

### Panel layout

<table>
  <tr>
    <th width="50%">Background on</th>
    <th width="50%">Background off, the card takes the theme's card background</th>
  </tr>
  <tr><td colspan="2"><b>Default elements</b></td></tr>
  <tr>
    <td><img src="images/panel_default.png" alt="Panel layout, default elements, background on"></td>
    <td><img src="images/panel_default_nobg.png" alt="Panel layout, default elements, background off"></td>
  </tr>
  <tr><td colspan="2"><b>All bars and values</b></td></tr>
  <tr>
    <td><img src="images/panel_all.png" alt="Panel layout, all bars and values, background on"></td>
    <td><img src="images/panel_all_nobg.png" alt="Panel layout, all bars and values, background off"></td>
  </tr>
  <tr><td colspan="2"><b>ApexCharts graph</b> with reset lines, a look ahead and the trend to the limit</td></tr>
  <tr>
    <td><img src="images/panel_graph.png" alt="Panel layout with ApexCharts graph, background on"></td>
    <td><img src="images/panel_graph_nobg.png" alt="Panel layout with ApexCharts graph, background off"></td>
  </tr>
</table>

### Hero layout

<table>
  <tr>
    <th width="50%">Background on</th>
    <th width="50%">Background off, the card takes the theme's card background</th>
  </tr>
  <tr><td colspan="2"><b>Default elements</b></td></tr>
  <tr>
    <td><img src="images/hero_default.png" alt="Hero layout, default elements, background on"></td>
    <td><img src="images/hero_default_nobg.png" alt="Hero layout, default elements, background off"></td>
  </tr>
  <tr><td colspan="2"><b>All bars and values</b></td></tr>
  <tr>
    <td><img src="images/hero_all.png" alt="Hero layout, all bars and values, background on"></td>
    <td><img src="images/hero_all_nobg.png" alt="Hero layout, all bars and values, background off"></td>
  </tr>
  <tr><td colspan="2"><b>Statistics graph</b>, built into Home Assistant</td></tr>
  <tr>
    <td><img src="images/hero_graph.png" alt="Hero layout with statistics graph, background on"></td>
    <td><img src="images/hero_graph_nobg.png" alt="Hero layout with statistics graph, background off"></td>
  </tr>
</table>

### Visual editor

<table>
  <tr>
    <th width="50%">Account, layout and elements</th>
    <th width="50%">Values and graph</th>
  </tr>
  <tr>
    <td><img src="images/editor_options.png" alt="Visual editor, account, layout and elements"></td>
    <td><img src="images/editor_graph.png" alt="Visual editor, values and graph options"></td>
  </tr>
</table>

## Configuration

The card ships a **visual editor** — no YAML required. Open the card's edit dialog and pick your
Clawdmeter **account**; every entity is filled in automatically (matched by the integration's
translation keys, so it is language‑independent). You can also choose the **layout**
(`panel` / `hero`), set an optional **title**, and toggle each element via checkboxes, grouped as:

- **General** — title, creature, header line, background, status chips, follow weekly window
- **Bars** — session, week, time‑to‑limit, Sonnet, Opus, model (weekly), extra usage,
  usage by surface
- **Values** — burn rate (5m / 30m), week pace, time to limit, limit ETA, buffer to reset,
  pace, peak today, session reset‑in
- **Graph** — graph card, time span, series (usage, burn rates, model), how the burn rates
  are scaled, and the ApexCharts extras

The "time‑to‑limit" bar tracks session usage toward the limit (severity‑coloured) and shows
the projected ETA, mirroring the ESPHome Clawdmeter. The card follows your Home Assistant
language, time format and number format (English and German included) and adapts to
light/dark themes. The editor shows the installed versions of the integration and the card.

On plans without a five‑hour limit (Ultra) the integration reports the weekly window in the
session sensors. With **follow weekly window** on (the default), the card then drops the
duplicate session bar, labels the remaining values by week and shows the week pace in place
of the five‑minute burn rate.

The graph is drawn by another card. The history and statistics graphs are built into Home
Assistant; Mini Graph Card and ApexCharts Card need to be installed. When one is missing,
the editor offers to install it (admins, Home Assistant 2026.11 and later) or links to it,
and the card falls back to the history graph. Burn rates and percentages differ in scale, so
the burn rates can share the scale, get their own scale on the right (Mini Graph,
ApexCharts) or a chart of their own below. Usage by surface needs ha‑clawdmeter 0.2.2 or
later.

With the **background** turned off, the card uses your theme's card background, so it fits a
light theme too.

### YAML (optional)

```yaml
type: custom:clawdmeter-card
layout: panel # or: hero
title: Clawdmeter # optional
graph: apex # optional: none, history, statistics, mini or apex
graph_hours: 24 # optional time span of the graph
rate_scale: axis # optional: shared, axis or chart
show: # optional per-element visibility
  background: true
  creature: true
  sonnet: false
  model: true # per-model weekly cap, for example Fable
  weekly: true # follow the weekly window on plans without a session limit
  g_burn: true # burn rates in the graph
# entity ids (session_usage, week_usage, time_to_limit, …) are filled by the editor
```

## Installation

### Marketplace (recommended)

Home Assistant 2026.11 and later ship the [Marketplace](https://www.home-assistant.io/integrations/marketplace/),
which replaces HACS. The card is a custom repository there, which needs a GitHub connection.

1. Go to **Settings** → **Marketplace** and select **Add from link**, or use the button at the top.
2. Enter `corgan2222/lovelace-clawdmeter` and select **Add**. If you are asked for the type,
   choose **Dashboard**.
3. Install **Clawdmeter Card**, then reload your browser.
4. Add the card to a dashboard. The visual editor fills in your Clawdmeter account automatically.

Updates show up under **Settings** → **Updates**. On older Home Assistant versions, add the
repository in HACS as a custom repository of category **Dashboard** instead.

You also need the [Clawdmeter integration](https://github.com/corgan2222/ha-clawdmeter) for the
underlying sensors.

### Manual

Copy `clawdmeter.js` to `config/www/` and add it as a dashboard resource
(`/local/clawdmeter.js`, type _JavaScript Module_), or load it via `lovelace.resources` /
`frontend.extra_module_url`.

## Credits

- [HermannBjorgvin/Clawdmeter](https://github.com/HermannBjorgvin/Clawdmeter) — the original creature and concept.
- [trickv/hass-claude-usage](https://github.com/trickv/hass-claude-usage) — the reference integration this build reworks.
- [esphome-modular-lvgl-buttons](https://github.com/corgan2222/esphome-modular-lvgl-buttons) — the ESPHome Clawdmeter display.
- [claudepix.vercel.app](https://claudepix.vercel.app/) — the pixel-art creature animations.

## License

[MIT](LICENSE)
