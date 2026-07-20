# Send Image Template Message with Kommunicate

Creates an image template message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Image Template Message](https://docs.kommunicate.io/docs/message-types#images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Conversation identifier to send the message into. |
| `message` | body | `string` | yes | Message text shown above the image template. |
| `fromUserName` | body | `string` | yes | Sender user ID. |
| `payloadJson` | body | `string<object>` | yes | Array of image objects from the official template format. |
