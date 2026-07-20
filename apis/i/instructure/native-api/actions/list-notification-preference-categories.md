# List Notification Preference Categories with Instructure

Retrieves notification preference categories from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/self/communication_channels/:communication_channel_id/notification_preference_categories`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Notification Preference Categories](https://developerdocs.instructure.com/services/canvas/resources/notification_preferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `communication_channel_id` | path | `string` | yes | The Canvas communication channel ID. |
