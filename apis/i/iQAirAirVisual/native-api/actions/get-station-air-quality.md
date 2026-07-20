# Get Station Air Quality with IQAir AirVisual

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/station`
- **Base URL:** `https://api.airvisual.com`
- **Official documentation:** [Get Station Air Quality](https://api-docs.iqair.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `station` | query | `string` | yes | Station name exactly as returned by the List Stations action. |
| `city` | query | `string` | yes | City name containing the requested station. |
| `state` | query | `string` | yes | State name containing the requested station. |
| `country` | query | `string` | yes | Country name containing the requested station. |
