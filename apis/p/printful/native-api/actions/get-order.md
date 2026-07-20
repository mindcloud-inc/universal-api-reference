# Get Order with Printful

Retrieves an order from your Printful account.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/{id}`
- **Base URL:** `https://api.printful.com`
- **Official documentation:** [Get Order](https://developers.printful.com/docs/#tag/Orders-API/operation/getOrderById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Printful order id or external id prefixed with @. |
