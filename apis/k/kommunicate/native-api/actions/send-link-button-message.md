# Send Link Button Message with Kommunicate

Creates a link button message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Link Button Message](https://docs.kommunicate.io/docs/message-types#link-button)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Conversation identifier to send the message into. |
| `message` | body | `string` | yes | Message text shown above the link buttons. |
| `fromUserName` | body | `string` | yes | Sender user ID. |
| `payloadJson` | body | `string<object>` | yes | Array of link button objects from the official template format. |
