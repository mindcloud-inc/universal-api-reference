# List Cart Items with Emporix Commerce Engine

Retrieves items in a cart from Emporix Commerce Engine.

## Endpoint

- **Method:** `GET`
- **Path:** `/cart/{tenantId}/carts/:cartId/items`
- **Base URL:** `https://api.emporix.io`
- **Official documentation:** [List Cart Items](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cartId` | path | `string` | yes | The unique ID of the cart whose items should be listed. |
