# Send HTML Content Message with Kommunicate

Creates an HTML content message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send HTML Content Message](https://docs.kommunicate.io/docs/message-types#html-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Conversation identifier to send the message into. |
| `message` | body | `string` | yes | HTML message content to send. |
| `fromUserName` | body | `string` | yes | Sender user ID. |
