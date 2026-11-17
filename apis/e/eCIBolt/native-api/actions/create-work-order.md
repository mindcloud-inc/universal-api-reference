# Create Work Order with ECI Bolt

## Endpoint

- **Method:** `POST`
- **Path:** `/open/v1/work_orders`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [Create Work Order](https://app.bolttech.net/api-docs/index.html#/Work_Orders/post_open_v1_work_orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `work_order` | body | `object` | no | — |
| `work_order.stage_id` | body | `number` | no | — |
| `work_order.work_order_type_id` | body | `number` | no | — |
| `work_order.reschedule_date` | body | `string` | no | — |
| `work_order.estimated_completion_date` | body | `string` | no | — |
| `work_order.completed_date` | body | `string` | no | — |
| `work_order.crew_notes` | body | `string` | no | — |
| `work_order.notes` | body | `string` | no | — |
| `work_order.job_id` | body | `number` | no | — |
| `work_order.appointment_start_time` | body | `string` | no | — |
| `work_order.appointment_end_time` | body | `string` | no | — |
| `work_order.assign_crew_ids[]` | body | `array<number>` | no | Send multiple values as a array. |
| `work_order.schedule_change_comment` | body | `string` | no | — |
| `work_order.schedule_change_reason_id` | body | `number` | no | — |
| `work_order.skip_schedule_rules` | body | `boolean` | no | — |
