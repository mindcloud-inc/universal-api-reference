# Update Conversation with Front

Updates an existing conversation in Front.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/conversations/:conversation_id`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Update Conversation](https://dev.frontapp.com/reference/update-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | — |
| `assignee_id` | body | `string` | no | ID of the teammate to assign the conversation to. |
| `inbox_id` | body | `string` | no | ID of the inbox to move the conversation to. |
| `status` | body | `list` | no | New status of the conversation. Accepted values: `archived`, `deleted`, `open`, `spam`. |
| `status_id` | body | `string` | no | Unique identifier of the status to set. |
| `tag_ids[]` | body | `array<string>` | no | List of tag IDs replacing the conversation tags. |
| `custom_fields` | body | `object` | no | Conversation custom fields object. |
