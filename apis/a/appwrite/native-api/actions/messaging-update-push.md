# Update push notification with Appwrite

Updates the push notification in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/messages/push/{messageId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update push notification](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Message ID. |
| `targets` | body | `string` | no | List of Targets IDs. |
| `topics` | body | `string` | no | List of Topic IDs. |
| `users` | body | `string` | no | List of User IDs. |
| `topics[]` | body | `array<string>` | no | List of Topic IDs. |
| `users[]` | body | `array<string>` | no | List of User IDs. |
| `targets[]` | body | `array<string>` | no | List of Targets IDs. |
| `title` | body | `string` | no | Title for push notification. |
| `body` | body | `string` | no | Body for push notification. |
| `data` | body | `object` | no | Additional Data for push notification. |
| `action` | body | `string` | no | Action for push notification. |
| `image` | body | `string` | no | Image for push notification. Must be a compound bucket ID to file ID of a jpeg, png, or bmp image in Appwrite Storage. It should be formatted as <BUCKET_ID>:<FILE_ID>. |
| `icon` | body | `string` | no | Icon for push notification. Available only for Android and Web platforms. |
| `sound` | body | `string` | no | Sound for push notification. Available only for Android and iOS platforms. |
| `color` | body | `string` | no | Color for push notification. Available only for Android platforms. |
| `tag` | body | `string` | no | Tag for push notification. Available only for Android platforms. |
| `badge` | body | `number` | no | Badge for push notification. Available only for iOS platforms. |
| `draft` | body | `boolean` | no | Is message a draft |
| `scheduledAt` | body | `string` | no | Scheduled delivery time for message in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. DateTime value must be in future. |
| `contentAvailable` | body | `boolean` | no | If set to true, the notification will be delivered in the background. Available only for iOS Platform. |
| `critical` | body | `boolean` | no | If set to true, the notification will be marked as critical. This requires the app to have the critical notification entitlement. Available only for iOS Platform. |
| `priority` | body | `string` | no | Set the notification priority. "normal" will consider device battery state and may send notifications later. "high" will always attempt to immediately deliver the notification. |
