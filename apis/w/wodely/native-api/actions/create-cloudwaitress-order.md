# Create CloudWaitress Order with Wodely

## Endpoint

- **Method:** `POST`
- **Path:** `/cloudwaitress/order`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Create CloudWaitress Order](https://www.wodely.com/project/cloudwaitress/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `secret` | body | `string` | no | CloudWaitress webhook secret value. |
| `event` | body | `string` | no | CloudWaitress webhook event identifier. |
| `event_id` | body | `string` | no | CloudWaitress webhook event ID. |
| `restaurant_id` | body | `string` | no | CloudWaitress restaurant identifier. |
| `data` | body | `object` | no | CloudWaitress webhook data object containing the order payload. |
