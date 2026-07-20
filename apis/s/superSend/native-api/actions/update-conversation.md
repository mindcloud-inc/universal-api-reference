# Update Conversation with SuperSend

Updates an existing conversation in SuperSend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/conversations/{id}`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Update Conversation](https://docs.supersend.io/docs/conversation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `is_archived` | body | `boolean` | no |
| `is_unread` | body | `boolean` | no |
| `mark_all_read` | body | `boolean` | no |
