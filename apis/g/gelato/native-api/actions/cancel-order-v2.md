# Cancel Order v2 with Gelato

Cancels an order in Gelato v2 by order reference ID.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.gelato.com/v2/order/cancel`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Cancel Order v2](https://dashboard.gelato.com/docs/orders/v2/cancel/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderReferenceId` | body | `string` | yes |
