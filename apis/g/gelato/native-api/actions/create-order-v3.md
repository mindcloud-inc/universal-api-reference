# Create Order v3 with Gelato

Creates an order in Gelato v3.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/orders`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Create Order v3](https://dashboard.gelato.com/docs/orders/v3/create/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderReferenceId` | body | `string` | yes |
| `customerReferenceId` | body | `string` | yes |
| `currency` | body | `string` | yes |
| `items[]` | body | `array<object>` | yes |
| `shippingAddress` | body | `object` | yes |
