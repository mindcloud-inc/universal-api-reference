# Ramp: Subscribe To Events

This actions is used in conjunction with the Verify Webhook Endpoint action to register a webhook event in Ramp

```
POST https://connect.mindcloud.co/v1/universal/ramp/latest/actions/subscribe-to-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ramp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ramp/latest/actions/subscribe-to-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpointURL": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ramp/latest/actions/subscribe-to-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpointURL": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpointURL` | string | yes | This is MindCloud's Webhook URL |
| `eventTypes[]` | array<string> | no | The event type IDs that the webhook subscribes to. Ref: https://docs.ramp.com/developer-api/v1/webhooks#available-events Default: `[\"transactions.ready_to_sync\"]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ramp API returns.

## Native endpoint

Through the native Ramp API, this operation is `POST webhooks` (base URL `https://api.ramp.com/developer/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-to-events.md) for the provider-specific parameters and requirements.

