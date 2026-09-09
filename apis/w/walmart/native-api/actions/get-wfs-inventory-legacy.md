# Get WFS Inventory (Legacy) with Walmart

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/fulfillment/inventory`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get WFS Inventory (Legacy)](https://developer.walmart.com/us-marketplace/reference/getwfsinventory#:~:text=Utilities-,WFS%20Inventory,-GET)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sku` | query | `string` | no |
| `fromModifiedDate` | query | `string` | no |
| `toModifiedDate` | query | `string` | no |
| `shipNodeType` | query | `string` | no |
