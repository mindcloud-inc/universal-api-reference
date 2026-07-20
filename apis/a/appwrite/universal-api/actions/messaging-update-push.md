# Appwrite: Update push notification

Updates the push notification in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-update-push
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-update-push" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-update-push', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | Message ID. |
| `targets` | string | no | List of Targets IDs. |
| `topics` | string | no | List of Topic IDs. |
| `users` | string | no | List of User IDs. |
| `topics[]` | array<string> | no | List of Topic IDs. |
| `users[]` | array<string> | no | List of User IDs. |
| `targets[]` | array<string> | no | List of Targets IDs. |
| `title` | string | no | Title for push notification. |
| `body` | string | no | Body for push notification. |
| `data` | object | no | Additional Data for push notification. |
| `action` | string | no | Action for push notification. |
| `image` | string | no | Image for push notification. Must be a compound bucket ID to file ID of a jpeg, png, or bmp image in Appwrite Storage. It should be formatted as <BUCKET_ID>:<FILE_ID>. |
| `icon` | string | no | Icon for push notification. Available only for Android and Web platforms. |
| `sound` | string | no | Sound for push notification. Available only for Android and iOS platforms. |
| `color` | string | no | Color for push notification. Available only for Android platforms. |
| `tag` | string | no | Tag for push notification. Available only for Android platforms. |
| `badge` | number | no | Badge for push notification. Available only for iOS platforms. |
| `draft` | boolean | no | Is message a draft |
| `scheduledAt` | string | no | Scheduled delivery time for message in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. DateTime value must be in future. |
| `contentAvailable` | boolean | no | If set to true, the notification will be delivered in the background. Available only for iOS Platform. |
| `critical` | boolean | no | If set to true, the notification will be marked as critical. This requires the app to have the critical notification entitlement. Available only for iOS Platform. |
| `priority` | string | no | Set the notification priority. "normal" will consider device battery state and may send notifications later. "high" will always attempt to immediately deliver the notification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "data": {},
      "deliveredAt": "string",
      "deliveredTotal": 1,
      "deliveryErrors": [
        "string"
      ],
      "providerType": "string",
      "scheduledAt": "string",
      "status": "string",
      "targets": [
        "string"
      ],
      "topics": [
        "string"
      ],
      "users": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Message creation time in ISO 8601 format. |
| `$id` | string | Message ID. |
| `$updatedAt` | string | Message update date in ISO 8601 format. |
| `data` | object | Data of the message. |
| `deliveredAt` | string | The time when the message was delivered. |
| `deliveredTotal` | number | Number of recipients the message was delivered to. |
| `deliveryErrors` | array<string> | Delivery errors if any. |
| `providerType` | string | Message provider type. |
| `scheduledAt` | string | The scheduled time for message. |
| `status` | string | Status of delivery. |
| `targets` | array<string> | Target IDs set as recipients. |
| `topics` | array<string> | Topic IDs set as recipients. |
| `users` | array<string> | User IDs set as recipients. |

## Native endpoint

Through the native Appwrite API, this operation is `PATCH /messaging/messages/push/{messageId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-update-push.md) for the provider-specific parameters and requirements.

