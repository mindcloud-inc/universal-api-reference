# Send Suggested Replies Message with Kommunicate

Creates a suggested replies message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Suggested Replies Message](https://docs.kommunicate.io/docs/message-types#suggested-replies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Conversation identifier to send the message into. |
| `message` | body | `string` | yes | Message text shown above the suggested replies. |
| `fromUserName` | body | `string` | yes | Sender user ID. |
| `payloadJson` | body | `string<object>` | yes | Array of suggested reply objects from the official template format. |
