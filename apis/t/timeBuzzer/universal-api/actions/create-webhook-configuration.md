# timeBuzzer: Create Webhook Configuration



```
POST https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-webhook-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-webhook-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "event": "string",
  "active": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-webhook-configuration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `url` | string | yes | The webhook target URL. |
| `event` | string | yes | The webhook event name. |
| `active` | boolean | yes | Whether the webhook is active. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native timeBuzzer API returns.

## Native endpoint

Through the native timeBuzzer API, this operation is `POST /open-api/webhooks` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-configuration.md) for the provider-specific parameters and requirements.

