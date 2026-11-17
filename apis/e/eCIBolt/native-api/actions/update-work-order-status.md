# Update Work Order Status with ECI Bolt

## Endpoint

- **Method:** `PATCH`
- **Path:** `/open/v1/work_orders/:id/statuses`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [Update Work Order Status](https://app.bolttech.net/api-docs/index.html#/Work_Orders/patch_open_v1_work_orders__id__statuses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Id of the work order. |
| `status` | body | `boolean` | no | — |
| `work_order_status_type_id` | body | `number` | no | — |
