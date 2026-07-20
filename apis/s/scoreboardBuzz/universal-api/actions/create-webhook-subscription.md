# Scoreboard Buzz: Create Webhook Subscription

Creates a webhook subscription in Scoreboard Buzz.

```
POST https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/create-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoreboard Buzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | HTTPS URL that should receive webhook payloads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "event_type": "string",
      "id": 1,
      "status": 1,
      "target_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number | Account ID that owns the subscription. |
| `created` | date | Creation timestamp. |
| `event_type` | string | Subscribed webhook event type. |
| `id` | number | Webhook subscription ID. |
| `status` | number | Provider status code for the subscription. |
| `target_url` | string | Webhook callback URL that will receive deliveries. |

## Native endpoint

Through the native Scoreboard Buzz API, this operation is `POST /webhooks/subscribe` (base URL `https://api.scoreboardbuzz.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription.md) for the provider-specific parameters and requirements.

