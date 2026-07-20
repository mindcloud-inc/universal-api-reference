# Create Location By Address From Body with Open Data DC

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2.2/locations/:zones/:geo`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Create Location By Address From Body](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Address string body value. |
| `zones` | path | `string` | yes | Comma-separated zones, for example ward,psa. |
| `geo` | path | `boolean` | yes | Whether to include geometry. |
