# Delete Order with Billit

Deletes an existing order from Billit.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/orders/:orderID`
- **Base URL:** `https://api.sandbox.billit.be`
- **Official documentation:** [Delete Order](https://docs.billit.be/reference/order_deleteorder-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderID` | path | `number` | yes | Billit OrderID to delete. |
