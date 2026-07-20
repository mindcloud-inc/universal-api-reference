# Get or Create Conversation with Twist

Finds a Twist conversation, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/get_or_create`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Get or Create Conversation](https://developer.twist.com/v3/#get-or-create-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_ids` | query | `string<number>` | yes | JSON-encoded list of user IDs, for example [10073,10076]. |
| `workspace_id` | query | `number` | yes | The id of the workspace. |
