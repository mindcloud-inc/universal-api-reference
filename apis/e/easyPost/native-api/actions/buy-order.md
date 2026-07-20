# Buy Order with EasyPost

Purchases an existing order in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/:id/buy`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Buy Order](https://docs.easypost.com/docs/orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carrier` | body | `string` | yes | Carrier to use when buying the order, such as FedEx. |
| `id` | path | `string` | yes | EasyPost Order ID, beginning with order_. |
| `service` | body | `string` | yes | Carrier service to use when buying the order. |
