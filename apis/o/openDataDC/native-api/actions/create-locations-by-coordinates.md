# Create Locations By Coordinates with Open Data DC

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2.2/locations/:latlong/:distance/:zones/:geo`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Create Locations By Coordinates](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latlong` | path | `string` | yes | Latitude and longitude, for example 38.888,-77.00. |
| `distance` | path | `string` | yes | Distance, for example 100ft. |
| `zones` | path | `string` | yes | Comma-separated zones, for example ward,psa. |
| `geo` | path | `boolean` | yes | Whether to include geometry. |
