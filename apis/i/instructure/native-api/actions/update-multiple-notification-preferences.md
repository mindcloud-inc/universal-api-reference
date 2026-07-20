# Update Multiple Notification Preferences with Instructure

Updates multiple notification preferences in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/communication_channels/:communication_channel_id/notification_preferences`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Multiple Notification Preferences](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `communication_channel_id` | path | `string` | yes | The Canvas communication channel ID. |
| `notification_preferences` | body | `object` | yes | Object map of notification codes to preference payloads, for example { "assignment_changed": { "frequency": "never" } }. |
