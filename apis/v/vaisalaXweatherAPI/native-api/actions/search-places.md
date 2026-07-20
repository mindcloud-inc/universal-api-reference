# Search Places with Vaisala Xweather

Finds places in Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/places/search`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Search Places](https://www.xweather.com/docs/weather-api/endpoints/places)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Structured Xweather query string, for example `name:seattle`. |
