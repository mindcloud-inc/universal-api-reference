# Create Reminder Message with Zoom Team Chat

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/messages/:messageId/reminder`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [Create Reminder Message](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/createReminderForMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The unique identifier of the message. |
| `to_contact` | query | `string` | no | The email address of the Zoom contact for the reminder. |
| `to_channel` | query | `string` | no | The ID of the Zoom channel for the reminder. |
