# Adjust Stock Quantities with SquareSpace

Updates stock quantities in Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/commerce/inventory/adjustments`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Adjust Stock Quantities](https://developers.squarespace.com/commerce-apis/inventory#adjust-stock-quantities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `decrementOperations[]` | body | `array<object>` | no | Operations to decrement finite stock quantities. |
| `decrementOperations[].quantity` | body | `number` | no | Quantity to decrement. |
| `decrementOperations[].variantId` | body | `list<string>` | no | Variant ID to decrement. |
| `idempotencyKey` | query | `string` | yes | Unique idempotency key for safe stock-adjustment retries. |
| `incrementOperations[]` | body | `array<object>` | no | Operations to increment finite stock quantities. |
| `incrementOperations[].quantity` | body | `number` | no | Quantity to increment. |
| `incrementOperations[].variantId` | body | `list<string>` | no | Variant ID to increment. |
| `setFiniteOperations[]` | body | `array<object>` | no | Operations to set finite stock quantities. |
| `setFiniteOperations[].quantity` | body | `number` | no | Finite quantity to set. |
| `setFiniteOperations[].variantId` | body | `list<string>` | no | Variant ID for finite stock set operation. |
| `setUnlimitedOperations[]` | body | `array<string>` | no | Variant IDs to set as unlimited stock. |
