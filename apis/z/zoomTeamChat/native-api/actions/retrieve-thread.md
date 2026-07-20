# Retrieve Thread with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/:userId/messages/:messageId/thread`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Retrieve Thread](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/retrieveThread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user. |
| `messageId` | path | `string` | yes | The unique identifier of the main message. |
| `to_channel` | query | `string` | no | The channel ID for the thread. |
| `to_contact` | query | `string` | no | The contact email, member ID, or user ID for the thread. |
| `from` | query | `string` | yes | The start timestamp of replies in ISO-8601 format. |
| `to` | query | `string` | no | The end timestamp of replies in ISO-8601 format. |
| `sort` | query | `string` | no | Sort order, such as desc or asc. |
