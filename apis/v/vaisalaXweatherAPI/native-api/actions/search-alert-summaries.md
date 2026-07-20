# Search Alert Summaries with Vaisala Xweather

Finds alert summaries in Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/summary/search`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Search Alert Summaries](https://www.xweather.com/docs/weather-api/endpoints/alerts-summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Structured Xweather query string for alert summary search. |
