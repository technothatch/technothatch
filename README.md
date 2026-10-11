# ADS-B tooling

Open-source toolkit around [dump1090](https://github.com/flightaware/dump1090) and [readsb](https://github.com/wiedehopf/readsb) ADS-B receivers. Every repository here is MIT-licensed, tested in CI, and tagged for search.

**New here?** [dump1090-stack](https://github.com/technothatch/dump1090-stack) runs a full receiver UI + metrics setup with one `docker compose up`. [dump1090-exporter](https://github.com/technothatch/dump1090-exporter) (Prometheus) and [dump1090-healthcheck](https://github.com/technothatch/dump1090-healthcheck) (watchdog) are the most-used single pieces.

## Run & operate

- [dump1090-stack](https://github.com/technothatch/dump1090-stack) — Docker Compose stack: readsb + tar1090 + exporter + Prometheus + Grafana + Alertmanager
- [dump1090-healthcheck](https://github.com/technothatch/dump1090-healthcheck) — watchdog for decoder freshness, rates and disk; Nagios/Prometheus output, auto-restart
- [dump1090-alerts](https://github.com/technothatch/dump1090-alerts) — rule engine firing webhooks, ntfy, Discord, Telegram, email and shell actions

## Metrics & data

- [dump1090-exporter](https://github.com/technothatch/dump1090-exporter) — Prometheus exporter (Go): messages, aircraft, signal, CPU, CPR, tracks
- [dump1090-influx](https://github.com/technothatch/dump1090-influx) — stream positions into InfluxDB 2.x or a Telegraf socket listener
- [dump1090-grafana](https://github.com/technothatch/dump1090-grafana) — importable Grafana dashboards for traffic, coverage and receiver health
- [dump1090-recorder](https://github.com/technothatch/dump1090-recorder) — long-term SQLite flight recorder with a query CLI (track, near, export)
- [dump1090-coverage](https://github.com/technothatch/dump1090-coverage) — coverage/range heatmaps, sector stats and offline HTML reports

## Feeds & networking

- [beast-relay](https://github.com/technothatch/beast-relay) — multi-consumer Beast fan-out proxy: one decoder port, many feeds
- [dump1090-geofence](https://github.com/technothatch/dump1090-geofence) — region filter proxy that shares a Beast/SBS feed without leaking aircraft outside your area
- [dump1090-to-mqtt](https://github.com/technothatch/dump1090-to-mqtt) — publish aircraft state to MQTT with Home Assistant discovery

## Interfaces

- [dump1090-dashboard](https://github.com/technothatch/dump1090-dashboard) — modern dependency-light Vite + TypeScript web UI for local decoders
- [adsb-tui](https://github.com/technothatch/adsb-tui) — live terminal radar and TUI
- [dump1090-cli](https://github.com/technothatch/dump1090-cli) — fast, pretty CLI for humans reading `aircraft.json`
- [dump1090-sdk](https://github.com/technothatch/dump1090-sdk) — typed TypeScript client library for the HTTP API

## Testing & decoding

- [dump1090-simulator](https://github.com/technothatch/dump1090-simulator) — deterministic synthetic ADS-B traffic (HTTP + Beast output)
- [dump1090-replay](https://github.com/technothatch/dump1090-replay) — replay recorded `aircraft.json` history for developing UIs and alerts
- [squawk-decoder](https://github.com/technothatch/squawk-decoder) — offline Mode A squawk, emitter category and ICAO type decoder with a live monitor

## Upstream projects these tools plug into

[flightaware/dump1090](https://github.com/flightaware/dump1090) · [wiedehopf/readsb](https://github.com/wiedehopf/readsb) · [wiedehopf/tar1090](https://github.com/wiedehopf/tar1090)
