# Update Message with Webex

Updates an existing message in Webex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/messages/:messageId`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Update Message](https://developer.webex.com/messaging/docs/api/v1/messages/update-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Message identifier. |
| `roomId` | body | `string` | yes | Room ID that contains the message being updated. |
| `text` | body | `string` | yes | Updated plain-text message body. |
