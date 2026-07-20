# Liveblocks: Get Inbox Notification

Retrieves an inbox notification from Liveblocks.

```
GET https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-inbox-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-inbox-notification?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-inbox-notification?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no | ID of the user. |

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

Through the native Liveblocks API, this operation is `GET /users/:userId/inbox-notifications/:inboxNotificationId` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox-notification.md) for the provider-specific parameters and requirements.

