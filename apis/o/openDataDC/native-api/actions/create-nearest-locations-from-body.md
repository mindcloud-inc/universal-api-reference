# Create Nearest Locations From Body with Open Data DC

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2.2/locations/:count/:geo`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Create Nearest Locations From Body](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latlong` | body | `string` | yes | Latitude/longitude string value in the request JSON object. Provider runtime expects the singular key `latlong`. |
| `count` | path | `number` | yes | Nearest location number. |
| `geo` | path | `boolean` | yes | Whether to include geometry. |
