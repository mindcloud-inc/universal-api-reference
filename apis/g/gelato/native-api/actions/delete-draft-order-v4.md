# Delete Draft Order v4 with Gelato

Deletes a draft order from Gelato v4.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v4/orders/{{orderId}}`
- **Base URL:** `https://order.gelatoapis.com`
- **Official documentation:** [Delete Draft Order v4](https://dashboard.gelato.com/docs/orders/v4/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Order ID for the draft order to delete. |
