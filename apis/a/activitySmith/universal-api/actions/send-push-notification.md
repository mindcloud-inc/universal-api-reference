# ActivitySmith: Send Push Notification

Sends a push notification in ActivitySmith.

```
POST https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/send-push-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivitySmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/send-push-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/send-push-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |
| `message` | string | no |  |
| `media` | string | no |  |
| `redirection` | string | no |  |
| `target` | object | no |  |
| `target.channels[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActivitySmith API returns.

## Native endpoint

Through the native ActivitySmith API, this operation is `POST /push-notification` (base URL `https://activitysmith.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-push-notification.md) for the provider-specific parameters and requirements.

