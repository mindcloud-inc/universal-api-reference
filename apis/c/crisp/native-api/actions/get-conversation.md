# Get Conversation with Crisp

Retrieves a conversation from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/conversation/:session_id`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Get Conversation](https://docs.crisp.chat/references/rest-api/v1/#get-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier. |
| `session_id` | path | `string` | yes | The conversation session identifier. |
