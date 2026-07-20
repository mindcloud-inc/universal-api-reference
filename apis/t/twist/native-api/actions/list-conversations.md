# List Conversations with Twist

Retrieves conversations from a Twist workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/get`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [List Conversations](https://developer.twist.com/v3/#get-all-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | If enabled, only archived conversations are returned. |
| `limit` | query | `number` | no | Limits the number of conversations returned. |
| `order_by` | query | `string` | no | Either desc or asc based on last_active. |
| `workspace_id` | query | `number` | yes | The id of the workspace. |
