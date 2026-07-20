# Cancel Order v4 with Gelato

Cancels an order in Gelato v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/orders/{{orderId}}:cancel`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Cancel Order v4](https://dashboard.gelato.com/docs/orders/v4/cancel/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderId` | path | `string` | yes |
