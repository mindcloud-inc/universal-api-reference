# PushAlert: Send Notification To Segment



```
POST https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/send-notification-to-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushAlert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/send-notification-to-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "segId": "string",
  "title": "string",
  "message": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/send-notification-to-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "segId": "string",
    "title": "string",
    "message": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `icon` | string | no | HTTPS icon URL for the notification. |
| `segId` | string | yes | PushAlert segment ID. |
| `title` | string | yes | Notification title. |
| `message` | string | yes | Notification message body. |
| `url` | string | yes | Destination URL when the notification is clicked. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | ID of the scheduled or sent notification. |
| `success` | boolean | Whether the segment notification request succeeded. |

## Native endpoint

Through the native PushAlert API, this operation is `POST /rest/v2/web-push/segment/:segId/send` (base URL `https://api.pushalert.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification-to-segment.md) for the provider-specific parameters and requirements.

