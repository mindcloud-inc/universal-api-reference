# Electricity Maps: Native API Reference

A consolidated summary of Electricity Maps's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://app.electricitymaps.com/developer-hub/api/getting-started
- **API base URL:** `https://api.electricitymaps.com/v4`

## Authentication

### API Key

Use an Electricity Maps API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
auth-token: <apiKey>
```

[Official authentication documentation](https://app.electricitymaps.com/developer-hub/api/getting-started)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Carbon Free Energy Forecast](actions/get-carbon-free-energy-forecast.md) | `GET /carbon-free-energy/forecast` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Carbon Free Energy History](actions/get-carbon-free-energy-history.md) | `GET /carbon-free-energy/history` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Carbon Intensity Forecast](actions/get-carbon-intensity-forecast.md) | `GET /carbon-intensity/forecast` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Carbon Intensity History](actions/get-carbon-intensity-history.md) | `GET /carbon-intensity/history` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Electricity Mix Forecast](actions/get-electricity-mix-forecast.md) | `GET /electricity-mix/forecast` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Electricity Mix History](actions/get-electricity-mix-history.md) | `GET /electricity-mix/history` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Fossil Carbon Intensity Forecast](actions/get-fossil-carbon-intensity-forecast.md) | `GET /carbon-intensity-fossil-only/forecast` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Fossil Carbon Intensity History](actions/get-fossil-carbon-intensity-history.md) | `GET /carbon-intensity-fossil-only/history` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Latest Carbon Free Energy](actions/get-latest-carbon-free-energy.md) | `GET /carbon-free-energy/latest` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Latest Carbon Intensity](actions/get-latest-carbon-intensity.md) | `GET /carbon-intensity/latest` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Latest Electricity Flows](actions/get-latest-electricity-flows.md) | `GET /electricity-flows/latest` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Latest Electricity Mix](actions/get-latest-electricity-mix.md) | `GET /electricity-mix/latest` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Latest Fossil Carbon Intensity](actions/get-latest-fossil-carbon-intensity.md) | `GET /carbon-intensity-fossil-only/latest` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Latest Renewable Energy](actions/get-latest-renewable-energy.md) | `GET /renewable-energy/latest` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Carbon Free Energy](actions/get-past-carbon-free-energy.md) | `GET /carbon-free-energy/past` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Carbon Intensity](actions/get-past-carbon-intensity.md) | `GET /carbon-intensity/past` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Electricity Mix](actions/get-past-electricity-mix.md) | `GET /electricity-mix/past` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Fossil Carbon Intensity](actions/get-past-fossil-carbon-intensity.md) | `GET /carbon-intensity-fossil-only/past` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Range Carbon Free Energy](actions/get-past-range-carbon-free-energy.md) | `GET /carbon-free-energy/past-range` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Range Carbon Intensity](actions/get-past-range-carbon-intensity.md) | `GET /carbon-intensity/past-range` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Range Electricity Mix](actions/get-past-range-electricity-mix.md) | `GET /electricity-mix/past-range` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Range Fossil Carbon Intensity](actions/get-past-range-fossil-carbon-intensity.md) | `GET /carbon-intensity-fossil-only/past-range` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Range Renewable Energy](actions/get-past-range-renewable-energy.md) | `GET /renewable-energy/past-range` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Past Renewable Energy](actions/get-past-renewable-energy.md) | `GET /renewable-energy/past` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Renewable Energy Forecast](actions/get-renewable-energy-forecast.md) | `GET /renewable-energy/forecast` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Renewable Energy History](actions/get-renewable-energy-history.md) | `GET /renewable-energy/history` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Updated Since](actions/get-updated-since.md) | `GET /updated-since` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [Get Zone](actions/get-zone.md) | `GET /zone` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [List Data Centers](actions/list-data-centers.md) | `GET /data-centers` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
| [List Zones](actions/list-zones.md) | `GET /zones` | [docs](https://app.electricitymaps.com/developer-hub/api/reference) |
