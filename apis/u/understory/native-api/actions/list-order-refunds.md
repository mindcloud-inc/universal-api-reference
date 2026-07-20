# List Order Refunds with Understory

Retrieves order refunds from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orders/{{orderId}}/refunds`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Order Refunds](https://developer.understory.io/apis/order/getrefunds.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The unique identifier of the order. |
