# Create Conversation Field with SparrowDesk

Creates a conversation field in SparrowDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/fields`
- **Base URL:** `https://api.sparrowdesk.com/v1`
- **Official documentation:** [Create Conversation Field](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/fields/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Conversation field description. |
| `name` | body | `string` | yes | Conversation field display name. |
| `type` | body | `string` | yes | Conversation field type, for example single_line_text. |
