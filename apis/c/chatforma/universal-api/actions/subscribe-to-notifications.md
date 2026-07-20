# Chatforma: Subscribe To Notifications

Creates a new notification subscription in Chatforma.

```
POST https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/subscribe-to-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatforma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/subscribe-to-notifications" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "formId": "string",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/subscribe-to-notifications', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "formId": "string",
    "targetUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes | Bot ID to subscribe notifications for |
| `formId` | string | yes | Form ID to subscribe notifications for |
| `targetUrl` | string | yes | Webhook URL that should receive notifications |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | no | Optional event to subscribe to |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chatforma API returns.

## Native endpoint

Through the native Chatforma API, this operation is `POST /subscribe-notification` (base URL `https://api.pro.chatforma.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-notifications.md) for the provider-specific parameters and requirements.

