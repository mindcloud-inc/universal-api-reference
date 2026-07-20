# Storm Glass: Native API Reference

A consolidated summary of Storm Glass's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.stormglass.io/
- **API base URL:** `https://api.stormglass.io/v2`

## Authentication

### API Key

Connect with your Storm Glass API key. Storm Glass expects the API key in the Authorization request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.stormglass.io/authentication.md)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Astronomy](actions/get-astronomy.md) | `GET /astronomy/point` | [docs](https://docs.stormglass.io/astronomy.md) |
| [Get Bio Data](actions/get-bio-data.md) | `GET /bio/point` | [docs](https://docs.stormglass.io/bio.md) |
| [Get Elevation](actions/get-elevation.md) | `GET /elevation/point` | [docs](https://docs.stormglass.io/elevation.md) |
| [Get Historical Weather](actions/get-historical-weather.md) | `GET /historical/point` | [docs](https://docs.stormglass.io/historical.md) |
| [Get Marine Forecast](actions/get-marine-forecast.md) | `GET /weather/point` | [docs](https://docs.stormglass.io/weather.md) |
| [Get Solar Data](actions/get-solar-data.md) | `GET /solar/point` | [docs](https://docs.stormglass.io/solar.md) |
| [Get Tide Extremes](actions/get-tide-extremes.md) | `GET /tide/extremes/point` | [docs](https://docs.stormglass.io/tide.md) |
| [Get Tide Sea Level](actions/get-tide-sea-level.md) | `GET /tide/sea-level/point` | [docs](https://docs.stormglass.io/tide.md) |
| [Get Weather Forecast](actions/get-weather-forecast.md) | `GET /weather/point` | [docs](https://docs.stormglass.io/weather.md) |
