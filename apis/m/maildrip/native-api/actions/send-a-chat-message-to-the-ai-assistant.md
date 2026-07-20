# Send a chat message to the AI assistant with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/chat`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Send a chat message to the AI assistant](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | The user's message to the AI assistant |
| `history[]` | body | `array<object>` | no | Previous conversation history for context Send multiple values as a array. |
