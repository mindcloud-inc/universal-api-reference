# Cancel Order v3 with Gelato

Cancels an order in Gelato v3.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/orders/{{orderId}}:cancel`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Cancel Order v3](https://dashboard.gelato.com/docs/orders/v3/cancel/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderId` | path | `string` | yes |
