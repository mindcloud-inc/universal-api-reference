# Quote Order v2 with Gelato

Retrieves shipping options and promise UIDs in Gelato v2.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.gelato.com/v2/quote`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Quote Order v2](https://dashboard.gelato.com/docs/orders/v2/quote/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order` | body | `object` | yes |
| `recipient` | body | `object` | yes |
| `products[]` | body | `array<object>` | yes |
