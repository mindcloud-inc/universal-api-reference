# Generate Checkout Link with Torque

## Endpoint

- **Method:** `POST`
- **Path:** `/checkout/generate-link`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Generate Checkout Link](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cart.items[]` | body | `array<object>` | yes | Cart items. Each item needs productId and quantity; variant and metadata are optional. |
| `customerData` | body | `object` | no | Optional customer object such as email, name, or metadata. |
| `options` | body | `object` | no | Optional checkout settings such as expiresIn or metadata. |
