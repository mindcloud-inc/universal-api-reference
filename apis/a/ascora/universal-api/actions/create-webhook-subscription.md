# Ascora: Create Webhook Subscription

Creates a new webhook subscription in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookUrl": "https://webhook.site/your-endpoint",
  "systemName": "Codex Stage 3",
  "hookEvent": "JobCreated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookUrl": "https://webhook.site/your-endpoint",
    "systemName": "Codex Stage 3",
    "hookEvent": "JobCreated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hookUrl` | string | yes | Full URL endpoint Ascora should call when the event is triggered. Example: `https://webhook.site/your-endpoint`. |
| `systemName` | string | yes | Name of the external system subscribing to the event. Example: `Codex Stage 3`. |
| `hookEvent` | string | yes | Name of the webhook event to subscribe to. Example: `JobCreated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriptionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriptionId` | string |  |

## Native endpoint

Through the native Ascora API, this operation is `POST /WebHooks` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription.md) for the provider-specific parameters and requirements.

