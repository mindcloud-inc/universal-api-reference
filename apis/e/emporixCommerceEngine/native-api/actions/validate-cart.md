# Validate Cart with Emporix Commerce Engine

Retrieves cart validation results from Emporix Commerce Engine.

## Endpoint

- **Method:** `GET`
- **Path:** `/cart/{tenantId}/carts/:cartId/validate`
- **Base URL:** `https://api.emporix.io`
- **Official documentation:** [Validate Cart](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cartId` | path | `string` | yes | The unique ID of the cart to validate. |
