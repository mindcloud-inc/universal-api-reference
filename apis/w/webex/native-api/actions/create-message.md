# Create Message with Webex

Creates a new message in Webex.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Create Message](https://developer.webex.com/messaging/docs/api/v1/messages/create-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | body | `string` | yes | Room to send the message to. |
| `text` | body | `string` | yes | Plain-text message body. |
