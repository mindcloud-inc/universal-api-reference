# Update Manufacturing Order with Katana

Updates an existing manufacturing order in Katana.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/manufacturing_orders/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Update Manufacturing Order](https://developer.katanamrp.com/reference/updatemanufacturingorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | manufacturing order id |
| `status` | body | `string` | no | Not updatable when manufacturing order status is DONE and location is deleted       or manufacturing_allowed is false. |
| `order_no` | body | `string` | no | Not updatable when manufacturing order status is DONE. |
| `variant_id` | body | `number` | no | Not updatable when manufacturing order status is DONE. |
| `location_id` | body | `number` | no | Not updatable when manufacturing order status is DONE. |
| `planned_quantity` | body | `number` | no | Not updatable when manufacturing order status is DONE. |
| `actual_quantity` | body | `number` | no | Not updatable when manufacturing order status is DONE. |
| `order_created_date` | body | `string` | no | — |
| `production_deadline_date` | body | `string` | no | Use only if automatic production deadline calculation for the factory location is switched OFF.       Not updatable when manufacturing order status is DONE.  Not updatable when manufacturing order status is DONE. |
| `additional_info` | body | `string` | no | — |
| `done_date` | body | `string` | no | — |
| `batch_transactions[]` | body | `array<object>` | no | Not updatable when manufacturing order status is DONE. |
| `batch_transactions[].quantity` | body | `number` | no | — |
| `batch_transactions[].batch_id` | body | `number` | no | — |
