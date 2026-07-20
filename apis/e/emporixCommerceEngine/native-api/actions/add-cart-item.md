# Add Cart Item with Emporix Commerce Engine

Adds an item to a cart in Emporix Commerce Engine.

## Endpoint

- **Method:** `POST`
- **Path:** `/cart/{tenantId}/carts/:cartId/items`
- **Base URL:** `https://api.emporix.io`
- **Official documentation:** [Add Cart Item](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cartId` | path | `string` | yes | The unique ID of the cart to add an item to. |
