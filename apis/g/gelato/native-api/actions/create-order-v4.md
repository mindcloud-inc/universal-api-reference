# Create Order v4 with Gelato

Creates an order in Gelato v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/orders`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Create Order v4](https://dashboard.gelato.com/docs/orders/v4/create/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderReferenceId` | body | `string` | yes |
| `customerReferenceId` | body | `string` | yes |
| `currency` | body | `string` | yes |
| `items[]` | body | `array<object>` | yes |
| `shippingAddress` | body | `object` | yes |
