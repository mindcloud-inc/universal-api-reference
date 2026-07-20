# Remove Conversation with Crisp

Deletes an existing conversation from Crisp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/website/:website_id/conversation/:session_id`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Remove Conversation](https://docs.crisp.chat/references/rest-api/v1/#remove-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `session_id` | path | `string` | yes | The conversation session identifier |
