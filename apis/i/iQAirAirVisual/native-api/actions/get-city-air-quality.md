# Get City Air Quality with IQAir AirVisual

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/city`
- **Base URL:** `https://api.airvisual.com`
- **Official documentation:** [Get City Air Quality](https://api-docs.iqair.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Country name exactly as returned by the List Countries action. |
| `state` | query | `string` | yes | State name exactly as returned by the List States action. |
| `city` | query | `string` | yes | City name exactly as returned by the List Cities action. |
