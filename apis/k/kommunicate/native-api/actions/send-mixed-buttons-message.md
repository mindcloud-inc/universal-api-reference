# Send Mixed Buttons Message with Kommunicate

Creates a mixed buttons message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Mixed Buttons Message](https://docs.kommunicate.io/docs/message-types#combine-different-type-of-buttons-with-single-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Conversation identifier to send the message into. |
| `message` | body | `string` | yes | Message text shown above the mixed buttons. |
| `fromUserName` | body | `string` | yes | Sender user ID. |
| `payloadJson` | body | `string<object>` | yes | Array of mixed button objects from the official template format. |
