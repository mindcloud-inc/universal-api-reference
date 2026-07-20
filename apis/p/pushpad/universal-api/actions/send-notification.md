# Pushpad: Send Notification

Sends a web push notification with Pushpad.

```
POST https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/send-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/send-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actions[]` | array<object> | no | Accepts multiple values as an array. |
| `badgeUrl` | string | no |  |
| `body` | string | yes |  |
| `customData` | string | no |  |
| `customMetrics[]` | array<string> | no | Accepts multiple values as an array. |
| `iconUrl` | string | no |  |
| `imageUrl` | string | no |  |
| `projectId` | number | yes |  |
| `requireInteraction` | boolean | no |  |
| `sendAt` | date | no |  |
| `silent` | boolean | no |  |
| `starred` | boolean | no |  |
| `tags[]` | array<string> | no | Accepts multiple values as an array. |
| `targetUrl` | string | no |  |
| `title` | string | no |  |
| `ttl` | number | no |  |
| `uids[]` | array<string> | no | Accepts multiple values as an array. |
| `urgent` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "scheduled": 1,
      "sendAt": "string",
      "uids": [
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
| `id` | number |  |
| `scheduled` | number |  |
| `sendAt` | string |  |
| `uids` | array<string> |  |

## Native endpoint

Through the native Pushpad API, this operation is `POST /projects/:project_id/notifications` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification.md) for the provider-specific parameters and requirements.

