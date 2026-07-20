# timeBuzzer: Update Webhook Configuration



```
PUT https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/update-webhook-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/update-webhook-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "url": "https://example.com",
  "event": "string",
  "active": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/update-webhook-configuration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "url": "https://example.com",
    "event": "string",
    "active": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The webhook ID. |
| `url` | string | yes | The webhook target URL. |
| `event` | string | yes | The webhook event name. |
| `active` | boolean | yes | Whether the webhook is active. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native timeBuzzer API returns.

## Native endpoint

Through the native timeBuzzer API, this operation is `PUT /open-api/webhooks/:id` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-configuration.md) for the provider-specific parameters and requirements.

