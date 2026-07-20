# Adjust Product Stock with Ecwid

Updates product stock in Ecwid.

## Endpoint

- **Method:** `PUT`
- **Path:** `/:storeId/products/:productId/inventory`
- **Base URL:** `https://app.ecwid.com/api/v3`
- **Official documentation:** [Adjust Product Stock](https://docs.ecwid.com/api-reference/rest-api/products/adjust-product-stock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `number` | yes | Ecwid product ID. |
| `quantityDelta` | body | `number` | yes | Quantity adjustment amount. |
