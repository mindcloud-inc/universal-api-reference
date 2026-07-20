# Update Notification Preferences By Category with Instructure

Updates notification preferences by category in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/communication_channels/:communication_channel_id/notification_preference_categories/:category`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Notification Preferences By Category](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | path | `string` | yes | The Canvas notification preference category. |
| `communication_channel_id` | path | `string` | yes | The Canvas communication channel ID. |
| `notification_preferences.frequency` | body | `string` | yes | The desired frequency for this notification category. |
