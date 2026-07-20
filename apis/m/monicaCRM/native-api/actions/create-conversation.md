# Create Conversation with Monica CRM

Creates a new conversation in Monica CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations`
- **Base URL:** `https://app.monicahq.com/api`
- **Official documentation:** [Create Conversation](https://www.monicahq.com/api/conversations)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_field_type_id` | body | `string` | yes |
| `contact_id` | body | `string` | yes |
| `happened_at` | body | `date` | yes |
