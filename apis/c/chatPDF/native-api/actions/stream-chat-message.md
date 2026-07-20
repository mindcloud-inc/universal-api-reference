# Stream Chat Message with ChatPDF

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/message`
- **Base URL:** `https://api.chatpdf.com/v1`
- **Official documentation:** [Stream Chat Message](https://www.chatpdf.com/docs/api/backend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceId` | body | `string` | yes | ChatPDF source ID to query. |
| `messages[]` | body | `array<object>` | yes | Conversation history array of { role, content } objects. Include all relevant prior messages for follow-up questions. |
