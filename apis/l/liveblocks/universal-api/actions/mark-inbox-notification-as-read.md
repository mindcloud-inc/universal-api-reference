# Liveblocks: Mark Inbox Notification As Read

Marks an inbox notification as read in Liveblocks.

```
PUT https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/mark-inbox-notification-as-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/mark-inbox-notification-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/mark-inbox-notification-as-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "activityData": {},
      "id": "string",
      "kind": "string",
      "notifiedAt": "string",
      "readAt": "string",
      "roomId": "string",
      "subjectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityData` | object |  |
| `id` | string |  |
| `kind` | string |  |
| `notifiedAt` | string |  |
| `readAt` | string |  |
| `roomId` | string |  |
| `subjectId` | string |  |

## Native endpoint

Through the native Liveblocks API, this operation is `POST /inbox-notifications/:inboxNotificationId/read` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-inbox-notification-as-read.md) for the provider-specific parameters and requirements.

