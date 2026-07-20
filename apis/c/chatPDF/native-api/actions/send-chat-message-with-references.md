# Send Chat Message With References with ChatPDF

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/message`
- **Base URL:** `https://api.chatpdf.com/v1`
- **Official documentation:** [Send Chat Message With References](https://www.chatpdf.com/docs/api/backend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceId` | body | `string` | yes | ChatPDF source ID to query. |
| `messages[]` | body | `array<object>` | yes | Conversation history array of { role, content } objects. Include all relevant prior messages for follow-up questions. |
