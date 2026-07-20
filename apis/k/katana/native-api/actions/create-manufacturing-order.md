# Create Manufacturing Order with Katana

Creates a new manufacturing order in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/manufacturing_orders`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Create Manufacturing Order](https://developer.katanamrp.com/reference/createmanufacturingorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | body | `string` | no | — |
| `order_no` | body | `string` | yes | — |
| `variant_id` | body | `number` | yes | — |
| `location_id` | body | `number` | yes | — |
| `planned_quantity` | body | `number` | yes | — |
| `actual_quantity` | body | `number` | no | — |
| `order_created_date` | body | `string` | no | — |
| `production_deadline_date` | body | `string` | no | Use only if automatic production deadline calculation for the factory location is switched OFF. |
| `additional_info` | body | `string` | no | — |
| `batch_transactions[]` | body | `array<object>` | no | — |
| `batch_transactions[].quantity` | body | `number` | no | — |
| `batch_transactions[].batch_id` | body | `number` | no | — |
