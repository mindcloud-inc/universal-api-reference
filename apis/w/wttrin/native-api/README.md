# wttr.in: Native API Reference

A consolidated summary of wttr.in's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://github.com/chubin/wttr.in
- **API base URL:** `https://wttr.in`

## Authentication

### No authentication

wttr.in endpoints are publicly accessible and do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://github.com/chubin/wttr.in)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Compact Weather Forecast JSON](actions/get-compact-weather-forecast-json.md) | `GET /[:location]` | [docs](https://github.com/chubin/wttr.in#json-output) |
| [Get Current Weather Summary](actions/get-current-weather-summary.md) | `GET /[:location]` | [docs](https://github.com/chubin/wttr.in#one-line-output) |
| [Get Moon Phase](actions/get-moon-phase.md) | `GET /[:moonDate]` | [docs](https://github.com/chubin/wttr.in#moon-phases) |
| [Get Weather Forecast JSON](actions/get-weather-forecast-json.md) | `GET /[:location]` | [docs](https://github.com/chubin/wttr.in#json-output) |
| [Get Weather Metrics](actions/get-weather-metrics.md) | `GET /[:location]` | [docs](https://github.com/chubin/wttr.in#prometheus-metrics-output) |
