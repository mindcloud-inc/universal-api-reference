# Create Task with LionWheel Delivery

Creates a new task in LionWheel Delivery.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/create`
- **Base URL:** `https://test.lionwheel.com/api/v1`
- **Official documentation:** [Create Task](https://github.com/lionwheel/api#create-a-delivery)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination_phone` | body | `string` | no | The destination recipient phone number. |
| `notes` | body | `string` | no | General delivery notes. |
| `original_order_id` | body | `string` | yes | Your external order ID for the task. |
| `pickup_at` | body | `string` | no | Pickup date in LionWheel's expected format. |
