# Get Spec with Walmart

Retrieve specifications for a specified Product Type or a set of Product Types.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/items/spec`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Spec](https://developer.walmart.com/us-marketplace/reference/getspec)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedType` | body | `string` | no | The type of feed, which specifies the nature of the update.  Example: `MP_WFS_ITEM` |
| `version` | body | `string` | no | Enter the item specification version. Example: `5.0.20250121-19_24_23-api` |
| `productTypes` | body | `string` | no | An item type with a specific set of attributes that define the product. Example: `Shirts`, `Shoes`, `Baby Blankets` Send multiple values as a array. |
