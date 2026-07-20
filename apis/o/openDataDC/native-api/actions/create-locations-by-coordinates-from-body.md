# Create Locations By Coordinates From Body with Open Data DC

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2.2/locations/:distance/:geo`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Create Locations By Coordinates From Body](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latlong` | body | `string` | yes | Latitude/longitude string value in the request JSON object. Provider runtime expects the singular key `latlong`. |
| `distance` | path | `string` | yes | Distance, for example 100ft. |
| `zones` | body | `string` | yes | Comma-delimited zone values, for example ward,psa. |
| `geo` | path | `boolean` | yes | Whether to include geometry. |
