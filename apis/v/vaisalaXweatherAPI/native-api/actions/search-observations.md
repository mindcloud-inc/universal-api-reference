# Search Observations with Vaisala Xweather

Finds observations in Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/observations/search`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Search Observations](https://www.xweather.com/docs/weather-api/endpoints/observations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Structured Xweather query string for observation search. |
