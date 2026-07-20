# List Messages with Twist

Retrieves messages from a Twist conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversation_messages/get`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [List Messages](https://developer.twist.com/v3/#get-all-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | query | `number` | yes | The id of the conversation. |
| `limit` | query | `number` | no | Limits the number of messages returned. |
| `order_by` | query | `string` | no | Either desc or asc based on obj_index. |
