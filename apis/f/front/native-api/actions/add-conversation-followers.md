# Add Conversation Followers with Front

Adds followers to a conversation in Front.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversation_id/followers`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Add Conversation Followers](https://dev.frontapp.com/reference/add-conversation-followers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The conversation ID. |
| `teammate_ids[]` | body | `array<string>` | yes | IDs of the teammates to add to the followers list. |
| `ignore_errors` | query | `boolean` | no | Whether to ignore invalid teammate IDs and continue adding valid ones. |
