# Get Item Associations with Walmart

Retrieve Shipping Templates and Fulfillment Centers associated with your item SKUs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/items/associations`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Item Associations](https://developer.walmart.com/us-marketplace/reference/getitemassociations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no | List of items whose associations need to be fetched. The list should not exceed 50 items per request. |
| `items[].sku` | body | `string` | no | An arbitrary alphanumeric unique ID, specified by the seller, which identifies each item. |
