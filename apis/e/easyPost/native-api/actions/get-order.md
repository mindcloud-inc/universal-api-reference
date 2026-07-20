# Get Order with EasyPost

Retrieves details for an order from EasyPost.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:id`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Get Order](https://docs.easypost.com/docs/orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Order ID, beginning with order_. |
