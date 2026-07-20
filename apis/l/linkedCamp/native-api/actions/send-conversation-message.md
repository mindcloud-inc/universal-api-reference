# Send Conversation Message with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/send-message`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Send Conversation Message](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | body | `string` | yes | Conversation identifier. |
| `content` | body | `string` | yes | Message content to send. |
