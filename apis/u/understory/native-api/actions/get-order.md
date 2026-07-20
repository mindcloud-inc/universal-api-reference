# Get Order with Understory

Retrieves an order from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orders/{{orderId}}`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [Get Order](https://developer.understory.io/apis/order/getorder.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The unique identifier of the order. |
