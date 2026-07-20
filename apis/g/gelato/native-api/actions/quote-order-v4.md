# Quote Order v4 with Gelato

Retrieves shipping quotes for order items in Gelato v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/orders:quote`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Quote Order v4](https://dashboard.gelato.com/docs/orders/v4/quote/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderReferenceId` | body | `string` | yes |
| `customerReferenceId` | body | `string` | yes |
| `currency` | body | `string` | yes |
| `recipient` | body | `object` | yes |
| `products[]` | body | `array<object>` | yes |
