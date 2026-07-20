# List Stations with IQAir AirVisual

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/stations`
- **Base URL:** `https://api.airvisual.com`
- **Official documentation:** [List Stations](https://api-docs.iqair.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | yes | City name exactly as returned by the List Cities action. |
| `state` | query | `string` | yes | State name exactly as returned by the List States action. |
| `country` | query | `string` | yes | Country name exactly as returned by the List Countries action. |
