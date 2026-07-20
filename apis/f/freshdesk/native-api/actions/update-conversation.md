# Update Conversation with Freshdesk

Updates an existing conversation in Freshdesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/:id`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Update Conversation](https://developers.freshdesk.com/api/#update_conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Freshdesk conversation ID. |
| `attachments[]` | body | `array<object>` | no | Conversation attachments |
| `body` | body | `string` | no | Updated conversation content in HTML |
