# Create Location By Address With Zones with Open Data DC

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2.2/locations/:address/:zones/:geo`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Create Location By Address With Zones](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | Address string value. |
| `zones` | path | `string` | yes | Comma-separated zones, for example ward,psa. |
| `geo` | path | `boolean` | yes | Whether to include geometry. |
