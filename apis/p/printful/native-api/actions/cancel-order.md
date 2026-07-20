# Cancel Order with Printful

Cancels an existing order in Printful.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orders/{id}`
- **Base URL:** `https://api.printful.com`
- **Official documentation:** [Cancel Order](https://developers.printful.com/docs/#tag/Orders-API/operation/cancelOrderById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Printful order id or external id prefixed with @. |
