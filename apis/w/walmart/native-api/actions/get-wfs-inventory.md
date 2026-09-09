# Get WFS Inventory with Walmart

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/wfs/inventory`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get WFS Inventory](https://developer.walmart.com/us-marketplace/reference/getwfsinventorydetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku` | query | `string` | no | Send multiple values as a array. |
| `shipNodeType` | query | `list<string>` | no | Filter results by ship-node type.  - Only supported value is `multichannel`. - Use this parameter only if you are a multi-channel seller. - When you send `shipNodeType`, you must also send `sku`. All other query parameters are ignored. - `sku` can be a single value or several SKUs separated by commas (for example, "sku1,sku2"). |
| `gtin` | query | `string` | no | — |
| `fromModifiedDate` | query | `string` | no | The start of the last modified date range. Returns only inventory records updated on or after this timestamp. Use 24-hour UTC format `YYYY-MM-DD HH:mm:ss` (for example, `2025-06-01 00:00:00`). |
| `toModifiedDate` | query | `string` | no | The end of the last-modified date range. Returns only inventory records updated on or before this timestamp. Use the same `YYYY-MM-DD HH:mm:ss` format as `fromModifiedDate`. |
