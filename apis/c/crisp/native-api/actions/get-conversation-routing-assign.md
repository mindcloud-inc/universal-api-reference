# Get Conversation Routing Assign with Crisp

Retrieves a conversation's routing assignment from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/conversation/:session_id/routing`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Get Conversation Routing Assign](https://docs.crisp.chat/references/rest-api/v1/#get-conversation-routing-assign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `session_id` | path | `string` | yes | The conversation session identifier |
