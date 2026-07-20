# Get Messages In Conversation with Crisp

Retrieves messages in a Crisp conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/conversation/:session_id/messages`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Get Messages In Conversation](https://docs.crisp.chat/references/rest-api/v1/#get-messages-in-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier. |
| `session_id` | path | `string` | yes | The conversation session identifier. |
| `timestamp_before` | query | `number` | no | Return messages before the given timestamp. |
