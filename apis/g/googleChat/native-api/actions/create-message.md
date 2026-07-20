# Create Message with Google Chat

Creates a message in a Google Chat space.

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/:space/messages`
- **Base URL:** `https://chat.googleapis.com/v1`
- **Official documentation:** [Create Message](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces.messages/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Enter only the space ID from the List Spaces result. If the result shows spaces/4Oe1TyAAAAE, enter 4Oe1TyAAAAE here. |
| `threadKey` | query | `string` | no | Optional thread key for replies or new threads. |
| `requestId` | query | `string` | no | Optional idempotency key for this message request. |
| `messageReplyOption` | query | `string` | no | Optional reply behavior for named spaces. |
| `messageId` | query | `string` | no | Optional custom message ID. |
| `text` | body | `string` | yes | Plain-text message body to send to the selected Google Chat space. With user OAuth, messages are sent as the connected Google user. |
