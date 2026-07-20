# Update Conversation with Superchat

Updates an existing conversation in Superchat.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/conversations/{conversation_id}`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Update Conversation](https://developers.superchat.com/reference/patchconversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The `id` of the conversation |
| `status` | body | `string` | no | The status of the conversation. |
| `snoozed_until` | body | `date` | no | Timestamp in UTC until when conversation is snoozed. |
| `assigned_users[]` | body | `array<string>` | no | Array of user_ids |
| `labels[]` | body | `array<string>` | no | Array of label_ids |
| `inbox_id` | body | `string` | no | Unique identifier of the inbox. Always bears prefix 'ib_' |
