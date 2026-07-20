# Patch Draft Order v3 with Gelato

Converts a draft order into a regular order in Gelato v3.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/orders/{{orderId}}`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Patch Draft Order v3](https://dashboard.gelato.com/docs/orders/v3/patch/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderId` | path | `string` | yes |
| `items[]` | body | `array<object>` | no |
