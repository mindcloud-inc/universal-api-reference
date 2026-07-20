# Pirate Weather: Native API Reference

A consolidated summary of Pirate Weather's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.pirateweather.net/en/latest/API/
- **API base URL:** `https://api.pirateweather.net`

## Authentication

### API Key

Connect with your Pirate Weather API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://docs.pirateweather.net/en/latest/API/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current Conditions](actions/get-current-conditions.md) | `GET /forecast/header-auth/:latitude,:longitude` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Daily Forecast](actions/get-daily-forecast.md) | `GET /forecast/header-auth/:latitude,:longitude` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Day/Night Forecast](actions/get-day-night-forecast.md) | `GET /forecast/header-auth/:latitude,:longitude` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Extended Hourly Forecast](actions/get-extended-hourly-forecast.md) | `GET /forecast/header-auth/:latitude,:longitude` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Forecast](actions/get-forecast.md) | `GET /forecast/header-auth/:latitude,:longitude` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Forecast With Extra Fields](actions/get-forecast-with-extra-fields.md) | `GET /forecast/header-auth/:latitude,:longitude` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Historical Current Conditions](actions/get-historical-current-conditions.md) | `GET https://timemachine.pirateweather.net/forecast/header-auth/:latitude,:longitude,:time` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Historical Daily Weather](actions/get-historical-daily-weather.md) | `GET https://timemachine.pirateweather.net/forecast/header-auth/:latitude,:longitude,:time` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Historical Detailed Weather](actions/get-historical-detailed-weather.md) | `GET https://timemachine.pirateweather.net/forecast/header-auth/:latitude,:longitude,:time` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Historical Hourly Weather](actions/get-historical-hourly-weather.md) | `GET https://timemachine.pirateweather.net/forecast/header-auth/:latitude,:longitude,:time` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Historical Weather](actions/get-historical-weather.md) | `GET https://timemachine.pirateweather.net/forecast/header-auth/:latitude,:longitude,:time` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Hourly Forecast](actions/get-hourly-forecast.md) | `GET /forecast/header-auth/:latitude,:longitude` | [docs](https://docs.pirateweather.net/en/latest/API/) |
| [Get Weather Alerts](actions/get-weather-alerts.md) | `GET /forecast/header-auth/:latitude,:longitude` | [docs](https://docs.pirateweather.net/en/latest/API/) |
