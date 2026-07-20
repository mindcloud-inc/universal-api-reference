# List Order Transactions with Understory

Retrieves order transactions from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orders/{{orderId}}/transactions`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Order Transactions](https://developer.understory.io/apis/order/gettransactions.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The unique identifier of the order. |
