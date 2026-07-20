# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-stormglass-io-48x48_1777646899369.png" alt="Storm Glass logo" width="28" height="28"> Storm Glass: Universal API

Storm Glass provides global weather, marine, tide, astronomy, solar, bio, historical weather, and elevation data by coordinate through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stormGlass/latest
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stormglass.io/
- **Vendor API docs:** https://docs.stormglass.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Astronomy](actions/get-astronomy.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormGlass/latest/actions/get-astronomy?connectionId=$CONNECTION_ID&lat=37.7749&lng=-122.4194" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Astronomy

| Action | Method | Description |
| --- | --- | --- |
| [Get Astronomy](actions/get-astronomy.md) | GET | Retrieves astronomy data from Storm Glass. |

### Biodata

| Action | Method | Description |
| --- | --- | --- |
| [Get Bio Data](actions/get-bio-data.md) | GET | Retrieves bio data from Storm Glass. |

### Elevation

| Action | Method | Description |
| --- | --- | --- |
| [Get Elevation](actions/get-elevation.md) | GET | Retrieves elevation data from Storm Glass. |

### Historicalweather

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Weather](actions/get-historical-weather.md) | GET | Retrieves historical weather data from Storm Glass. |

### Marineforecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Marine Forecast](actions/get-marine-forecast.md) | GET | Retrieves marine weather forecasts from Storm Glass. |

### Solardata

| Action | Method | Description |
| --- | --- | --- |
| [Get Solar Data](actions/get-solar-data.md) | GET | Retrieves solar data from Storm Glass. |

### Tideextreme

| Action | Method | Description |
| --- | --- | --- |
| [Get Tide Extremes](actions/get-tide-extremes.md) | GET | Retrieves tide extremes from Storm Glass. |

### Tidesealevel

| Action | Method | Description |
| --- | --- | --- |
| [Get Tide Sea Level](actions/get-tide-sea-level.md) | GET | Retrieves tide sea-level data from Storm Glass. |

### Weatherforecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Weather Forecast](actions/get-weather-forecast.md) | GET | Retrieves weather forecasts from Storm Glass. |

