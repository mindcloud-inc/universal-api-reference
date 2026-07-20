# ReplyCX: Set Events Webhook



```
PUT https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/set-events-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReplyCX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/set-events-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookUrl": "https://example.com",
  "subscribed_events": {},
  "isEnabled": true,
  "token": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/set-events-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookUrl": "https://example.com",
    "subscribed_events": {},
    "isEnabled": true,
    "token": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookUrl` | string | yes |  |
| `subscribed_events` | list<object> | yes | List of ReplyCX event subscriptions as objects with keys `key` and `is_subscribed`. |
| `isEnabled` | boolean | yes |  |
| `token` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ReplyCX API returns.

## Native endpoint

Through the native ReplyCX API, this operation is `POST /v1/accounts/:account_id/webhook` (base URL `https://api.reply.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-events-webhook.md) for the provider-specific parameters and requirements.

