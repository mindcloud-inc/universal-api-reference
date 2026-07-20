# Confirm Order with Printful

Confirms a draft Printful order for fulfillment.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/{id}/confirm`
- **Base URL:** `https://api.printful.com`
- **Official documentation:** [Confirm Order](https://developers.printful.com/docs/#tag/Orders-API/operation/confirmOrderById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Printful order id or external id prefixed with @. |
