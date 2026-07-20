# Update Conversation with Monica CRM

Updates an existing conversation in Monica CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/:conversationId`
- **Base URL:** `https://app.monicahq.com/api`
- **Official documentation:** [Update Conversation](https://www.monicahq.com/api/conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | — |
| `happened_at` | body | `date` | yes | — |
| `contact_field_type_id` | body | `string` | yes | The contact field type ID associated with the conversation. |
