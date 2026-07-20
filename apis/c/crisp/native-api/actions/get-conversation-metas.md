# Get Conversation Metas with Crisp

Retrieves a conversation's metadata from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/conversation/:session_id/meta`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Get Conversation Metas](https://docs.crisp.chat/references/rest-api/v1/#get-conversation-metas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `session_id` | path | `string` | yes | The conversation session identifier |
