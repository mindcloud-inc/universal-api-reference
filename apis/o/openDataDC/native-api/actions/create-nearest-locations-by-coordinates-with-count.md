# Create Nearest Locations By Coordinates With Count with Open Data DC

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2.2/locations/:latlong/:count/:zones/:geo`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Create Nearest Locations By Coordinates With Count](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latlong` | path | `string` | yes | Latitude and longitude, for example 38.888,-77.00. |
| `count` | path | `number` | yes | Nearest location number. |
| `zones` | path | `string` | yes | Comma-separated zones, for example ward,psa. |
| `geo` | path | `boolean` | yes | Whether to include geometry. |
