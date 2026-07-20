# Patch Draft Order v4 with Gelato

Converts a draft order into a regular order in Gelato v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v4/orders/{{orderId}}`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Patch Draft Order v4](https://dashboard.gelato.com/docs/orders/v4/patch/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderId` | path | `string` | yes |
| `items[]` | body | `array<object>` | no |
