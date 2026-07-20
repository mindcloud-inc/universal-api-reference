# Get City Ranking with IQAir AirVisual

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/city_ranking`
- **Base URL:** `https://api.airvisual.com`
- **Official documentation:** [Get City Ranking](https://api-docs.iqair.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Optional ranking order: asc for cleanest cities or desc for most polluted cities. |
| `country` | query | `string` | no | Optional country filter. Allowed documented values include Thailand, USA, and Canada. |
