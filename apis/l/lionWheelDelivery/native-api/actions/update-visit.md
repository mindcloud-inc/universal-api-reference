# Update Visit with LionWheel Delivery

Updates an existing visit in LionWheel Delivery.

## Endpoint

- **Method:** `PUT`
- **Path:** `/visits/:visit_id`
- **Base URL:** `https://test.lionwheel.com/api/v1`
- **Official documentation:** [Update Visit](https://github.com/lionwheel/api#update-visit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_id` | body | `string` | no | Driver to assign to the visit. |
| `visit_at` | body | `string` | no | Visit date in LionWheel's expected format. |
| `visit_id` | path | `string` | yes | The LionWheel visit ID. |
