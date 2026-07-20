# Find Tasks by Order ID with LionWheel Delivery

Finds tasks in LionWheel Delivery by order ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/by_order_id/:order_id`
- **Base URL:** `https://test.lionwheel.com/api/v1`
- **Official documentation:** [Find Tasks by Order ID](https://github.com/lionwheel/api#get-tasks-by-order-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | The external order ID to search for. |
