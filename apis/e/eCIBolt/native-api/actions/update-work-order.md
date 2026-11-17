# Update Work Order with ECI Bolt

## Endpoint

- **Method:** `PATCH`
- **Path:** `/open/v1/work_orders/:id`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [Update Work Order](https://app.bolttech.net/api-docs/index.html#/Work_Orders/patch_open_v1_work_orders__id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Id of the work order. |
| `work_order` | body | `object` | no | — |
| `work_order.stage_id` | body | `number` | no | — |
| `work_order.work_order_type_id` | body | `number` | no | — |
| `work_order.reschedule_date` | body | `string` | no | — |
| `work_order.estimated_completion_date` | body | `string` | no | — |
| `work_order.completed_date` | body | `string` | no | — |
| `work_order.notes` | body | `string` | no | — |
| `work_order.job_id` | body | `number` | no | — |
| `work_order.appointment_start_time` | body | `string` | no | — |
| `work_order.appointment_end_time` | body | `string` | no | — |
| `work_order.assign_crew_ids[]` | body | `array<number>` | no | Send multiple values as a array. |
| `work_order.unassign_crew_ids[]` | body | `array<number>` | no | Send multiple values as a array. |
| `work_order.schedule_change_comment` | body | `string` | no | — |
| `work_order.schedule_change_reason_id` | body | `number` | no | — |
| `work_order.skip_schedule_rules` | body | `boolean` | no | — |
| `etag` | body | `string` | yes | Use the etag returned by a fresh Get request to avoid overwriting a newer record. |
