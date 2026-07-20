# List Order Line Items with Understory

Retrieves order line items from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orders/{{orderId}}/line-items`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Order Line Items](https://developer.understory.io/apis/order/getlineitems.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The unique identifier of the order. |
