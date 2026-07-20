# Get Conversation State with Crisp

Retrieves a conversation's state from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/conversation/:session_id/state`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Get Conversation State](https://docs.crisp.chat/references/rest-api/v1/#get-conversation-state)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `session_id` | path | `string` | yes | The conversation session identifier |
