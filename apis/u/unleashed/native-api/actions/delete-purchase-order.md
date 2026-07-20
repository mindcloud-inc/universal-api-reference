# Delete Purchase Order with Unleashed

Deletes an existing purchase order from Unleashed.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/PurchaseOrders/:orderGuid`
- **Base URL:** `https://api.unleashedsoftware.com`
- **Official documentation:** [Delete Purchase Order](https://apidocs.unleashedsoftware.com/Purchases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderGuid` | path | `string` | yes | The Unleashed purchase order GUID. |
