# Send Channel Message with Notify

Creates a new message in a Notify channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/:channelId`
- **Base URL:** `https://notify.run`
- **Official documentation:** [Send Channel Message](https://notify.run)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | no | Optional URL to open when the notification is clicked. |
| `channelId` | path | `string` | no | A Notify channel token or ID. |
| `message` | body | `string` | no | The notification text to send. |
