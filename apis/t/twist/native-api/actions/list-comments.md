# List Comments with Twist

Retrieves comments from a Twist thread.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/get`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [List Comments](https://developer.twist.com/v3/#get-all-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Limits the number of comments returned. |
| `order_by` | query | `string` | no | Either desc or asc based on obj_index. |
| `thread_id` | query | `number` | yes | The id of the thread. |
