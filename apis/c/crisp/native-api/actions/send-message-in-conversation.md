# Send Message In Conversation with Crisp

Sends a message in a Crisp conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/website/:website_id/conversation/:session_id/message`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Send Message In Conversation](https://docs.crisp.chat/references/rest-api/v1/#send-a-message-in-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `session_id` | path | `string` | yes | The conversation session identifier |
| `type` | body | `string` | yes | Message type |
| `from` | body | `list` | yes | Message sender Accepted values: `operator`, `user`. |
| `origin` | body | `list` | yes | Message origin Accepted values: `chat`, `email`, `urn:*`. |
| `content` | body | `string` | yes | Message content |
