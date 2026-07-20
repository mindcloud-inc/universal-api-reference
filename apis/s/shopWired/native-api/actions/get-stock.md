# Retrieve stock quantity with ShopWired

Retrieves stock quantities from ShopWired by SKU.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [Retrieve stock quantity](https://shopwired.readme.io/reference/getstock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku` | query | `string` | yes | The SKU code for the product or product variation. |
