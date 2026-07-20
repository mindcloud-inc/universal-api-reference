# List Notification Preferences with Instructure

Retrieves notification preferences from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/self/communication_channels/:communication_channel_id/notification_preferences`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Notification Preferences](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `communication_channel_id` | path | `string` | yes | The Canvas communication channel ID. |
