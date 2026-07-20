# Delete Order with MailBluster

Deletes an existing order from MailBluster.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orders/:orderId`
- **Base URL:** `https://api.mailbluster.com/api`
- **Official documentation:** [Delete Order](https://app.mailbluster.com/api-doc/orders/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Unique order ID to delete. |
