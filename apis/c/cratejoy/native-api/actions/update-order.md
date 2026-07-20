# Update Order with Cratejoy

Updates an existing order in Cratejoy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/orders/:orderId/`
- **Base URL:** `https://api.cratejoy.com`
- **Official documentation:** [Update Order](https://docs.cratejoy.com/reference/order-methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | The Cratejoy order ID. |
| `note` | body | `string` | no | A note for the order. |
