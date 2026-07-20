# Update Task with LionWheel Delivery

Updates an existing task in LionWheel Delivery.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:task_id/update`
- **Base URL:** `https://test.lionwheel.com/api/v1`
- **Official documentation:** [Update Task](https://github.com/lionwheel/api#update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pickup_at` | body | `string` | no | Pickup date for the task. |
| `task_id` | path | `string` | yes | The LionWheel task ID. |
| `status` | body | `number` | no | Task status code: UNASSIGNED=0, ASSIGNED=1, ACTIVE=2, COMPLETED=3, CANCELED=4, ROUNDTRIP_DELIVERED=5, FAILED=8. |
