# Validate External Order with Fourthwall

Validates an external order in Fourthwall before creation.

## Endpoint

- **Method:** `POST`
- **Path:** `/open-api/v1.0/external-orders/validate`
- **Base URL:** `https://api.fourthwall.com`
- **Official documentation:** [Validate External Order](https://docs.fourthwall.com/api-reference/platform/external-orders/validate-external-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | yes | Array of external order items to validate. Each item requires offerId, variantId, and quantity. |
| `shippingAddress` | body | `object` | yes | Shipping address object. Required fields: firstName, lastName, address1, city, zip, and country. address2, state, and phone are optional. |
