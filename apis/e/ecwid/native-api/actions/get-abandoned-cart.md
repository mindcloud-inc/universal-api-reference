# Get Abandoned Cart with Ecwid

Retrieves an abandoned cart from Ecwid.

## Endpoint

- **Method:** `GET`
- **Path:** `/:storeId/carts/:cartId`
- **Base URL:** `https://app.ecwid.com/api/v3`
- **Official documentation:** [Get Abandoned Cart](https://docs.ecwid.com/api-reference/rest-api/orders/abandonned-carts/get-abandoned-cart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cartId` | path | `number` | yes | Ecwid cart ID. |
