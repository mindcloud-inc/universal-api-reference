# Retire an Item with Walmart

Permanently retire an item identified by its SKU.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/items/:sku`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Retire an Item](https://developer.walmart.com/us-marketplace/reference/retireanitem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku` | path | `string` | yes | An arbitrary alphanumeric unique ID, specified by the seller, which identifies each item. |
