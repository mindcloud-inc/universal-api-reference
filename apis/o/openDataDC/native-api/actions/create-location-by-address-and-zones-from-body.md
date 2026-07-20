# Create Location By Address And Zones From Body with Open Data DC

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2.2/locations/:geo`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Create Location By Address And Zones From Body](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Address string in the request JSON object. |
| `geo` | path | `boolean` | yes | Whether to include geometry. |
| `zones` | body | `string` | yes | Comma-delimited zone values, for example ward,psa. |
