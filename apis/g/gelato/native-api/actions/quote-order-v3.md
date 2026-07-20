# Quote Order v3 with Gelato

Retrieves shipping quotes for order items in Gelato v3.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/orders:quote`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Quote Order v3](https://dashboard.gelato.com/docs/orders/v3/quote/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderReferenceId` | body | `string` | yes |
| `customerReferenceId` | body | `string` | yes |
| `currency` | body | `string` | yes |
| `recipient` | body | `object` | yes |
| `products[]` | body | `array<object>` | yes |
