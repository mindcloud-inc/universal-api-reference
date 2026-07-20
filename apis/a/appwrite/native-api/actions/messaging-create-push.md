# Create push notification with Appwrite

Creates a new push notification in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/messages/push`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create push notification](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | body | `string` | yes | Message ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `targets` | body | `string` | no | List of Targets IDs. |
| `topics` | body | `string` | no | List of Topic IDs. |
| `users` | body | `string` | no | List of User IDs. |
| `title` | body | `string` | no | Title for push notification. |
| `body` | body | `string` | no | Body for push notification. |
| `topics[]` | body | `array<string>` | no | List of Topic IDs. |
| `users[]` | body | `array<string>` | no | List of User IDs. |
| `targets[]` | body | `array<string>` | no | List of Targets IDs. |
| `data` | body | `object` | no | Additional key-value pair data for push notification. |
| `action` | body | `string` | no | Action for push notification. |
| `image` | body | `string` | no | Image for push notification. Must be a compound bucket ID to file ID of a jpeg, png, or bmp image in Appwrite Storage. It should be formatted as <BUCKET_ID>:<FILE_ID>. |
| `icon` | body | `string` | no | Icon for push notification. Available only for Android and Web Platform. |
| `sound` | body | `string` | no | Sound for push notification. Available only for Android and iOS Platform. |
| `color` | body | `string` | no | Color for push notification. Available only for Android Platform. |
| `tag` | body | `string` | no | Tag for push notification. Available only for Android Platform. |
| `badge` | body | `number` | no | Badge for push notification. Available only for iOS Platform. |
| `draft` | body | `boolean` | no | Is message a draft |
| `scheduledAt` | body | `string` | no | Scheduled delivery time for message in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. DateTime value must be in future. |
| `contentAvailable` | body | `boolean` | no | If set to true, the notification will be delivered in the background. Available only for iOS Platform. |
| `critical` | body | `boolean` | no | If set to true, the notification will be marked as critical. This requires the app to have the critical notification entitlement. Available only for iOS Platform. |
| `priority` | body | `string` | no | Set the notification priority. "normal" will consider device state and may not deliver notifications immediately. "high" will always attempt to immediately deliver the notification. |
