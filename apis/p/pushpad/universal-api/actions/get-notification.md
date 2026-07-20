# Pushpad: Get Notification

Retrieves a Pushpad notification and its stats.

```
GET https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/get-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/get-notification?connectionId=$CONNECTION_ID&notificationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "notificationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/get-notification?${params}`, {
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
| `notificationId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        "string"
      ],
      "badgeUrl": "https://example.com",
      "body": "string",
      "createdAt": "string",
      "customData": "string",
      "customMetrics": [
        "string"
      ],
      "iconUrl": "https://example.com",
      "id": 1,
      "projectId": 1,
      "requireInteraction": true,
      "scheduled": true,
      "sendAt": "string",
      "silent": true,
      "starred": true,
      "tags": [
        "string"
      ],
      "targetUrl": "https://example.com",
      "title": "string",
      "ttl": 1,
      "uids": [
        "string"
      ],
      "urgent": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array |  |
| `badgeUrl` | string |  |
| `body` | string |  |
| `createdAt` | string |  |
| `customData` | string |  |
| `customMetrics` | array |  |
| `iconUrl` | string |  |
| `id` | number |  |
| `projectId` | number |  |
| `requireInteraction` | boolean |  |
| `scheduled` | boolean |  |
| `sendAt` | string |  |
| `silent` | boolean |  |
| `starred` | boolean |  |
| `tags` | array<string> |  |
| `targetUrl` | string |  |
| `title` | string |  |
| `ttl` | number |  |
| `uids` | array<string> |  |
| `urgent` | boolean |  |

## Native endpoint

Through the native Pushpad API, this operation is `GET /notifications/:notification_id` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification.md) for the provider-specific parameters and requirements.

