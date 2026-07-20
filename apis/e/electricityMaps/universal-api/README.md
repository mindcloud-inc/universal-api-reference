# <img src="https://images.mindcloud.co/apps/icons/electricity-maps_1776093362179.png" alt="Electricity Maps logo" width="28" height="28"> Electricity Maps: Universal API

Electricity Maps provides real-time, historical, and forecasted electricity and carbon data by zone, geolocation, and data center region.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/electricityMaps/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.electricitymaps.com
- **Vendor API docs:** https://app.electricitymaps.com/developer-hub/api/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Latest Carbon Intensity](actions/get-latest-carbon-intensity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-latest-carbon-intensity?connectionId=$CONNECTION_ID&zone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Zone](actions/get-zone.md) | GET |  |
| [List Data Centers](actions/list-data-centers.md) | GET |  |
| [List Zones](actions/list-zones.md) | GET |  |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Carbon Free Energy Forecast](actions/get-carbon-free-energy-forecast.md) | GET |  |
| [Get Carbon Free Energy History](actions/get-carbon-free-energy-history.md) | GET |  |
| [Get Carbon Intensity Forecast](actions/get-carbon-intensity-forecast.md) | GET |  |
| [Get Carbon Intensity History](actions/get-carbon-intensity-history.md) | GET |  |
| [Get Electricity Mix Forecast](actions/get-electricity-mix-forecast.md) | GET |  |
| [Get Electricity Mix History](actions/get-electricity-mix-history.md) | GET |  |
| [Get Fossil Carbon Intensity Forecast](actions/get-fossil-carbon-intensity-forecast.md) | GET |  |
| [Get Fossil Carbon Intensity History](actions/get-fossil-carbon-intensity-history.md) | GET |  |
| [Get Latest Carbon Free Energy](actions/get-latest-carbon-free-energy.md) | GET |  |
| [Get Latest Carbon Intensity](actions/get-latest-carbon-intensity.md) | GET |  |
| [Get Latest Electricity Flows](actions/get-latest-electricity-flows.md) | GET |  |
| [Get Latest Electricity Mix](actions/get-latest-electricity-mix.md) | GET |  |
| [Get Latest Fossil Carbon Intensity](actions/get-latest-fossil-carbon-intensity.md) | GET |  |
| [Get Latest Renewable Energy](actions/get-latest-renewable-energy.md) | GET |  |
| [Get Past Carbon Free Energy](actions/get-past-carbon-free-energy.md) | GET |  |
| [Get Past Carbon Intensity](actions/get-past-carbon-intensity.md) | GET |  |
| [Get Past Electricity Mix](actions/get-past-electricity-mix.md) | GET |  |
| [Get Past Fossil Carbon Intensity](actions/get-past-fossil-carbon-intensity.md) | GET |  |
| [Get Past Range Carbon Free Energy](actions/get-past-range-carbon-free-energy.md) | GET |  |
| [Get Past Range Carbon Intensity](actions/get-past-range-carbon-intensity.md) | GET |  |
| [Get Past Range Electricity Mix](actions/get-past-range-electricity-mix.md) | GET |  |
| [Get Past Range Fossil Carbon Intensity](actions/get-past-range-fossil-carbon-intensity.md) | GET |  |
| [Get Past Range Renewable Energy](actions/get-past-range-renewable-energy.md) | GET |  |
| [Get Past Renewable Energy](actions/get-past-renewable-energy.md) | GET |  |
| [Get Renewable Energy Forecast](actions/get-renewable-energy-forecast.md) | GET |  |
| [Get Renewable Energy History](actions/get-renewable-energy-history.md) | GET |  |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Get Updated Since](actions/get-updated-since.md) | GET |  |

