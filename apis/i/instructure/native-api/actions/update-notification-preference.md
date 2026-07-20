# Update Notification Preference with Instructure

Updates a notification preference in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/communication_channels/:communication_channel_id/notification_preferences/:notification`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Notification Preference](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `communication_channel_id` | path | `string` | yes | The Canvas communication channel ID. |
| `notification` | path | `string` | yes | The Canvas notification code. |
| `notification_preferences.frequency` | body | `string` | yes | The desired frequency for this notification. |
