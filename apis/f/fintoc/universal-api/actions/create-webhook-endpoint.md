# Fintoc: Create Webhook Endpoint

Creates a webhook endpoint in Fintoc.

```
POST https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/webhooks/fintoc",
  "enabledEvents": "account.refresh_intent.succeeded"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-webhook-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/webhooks/fintoc",
    "enabledEvents": "account.refresh_intent.succeeded"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public HTTPS endpoint that receives Fintoc webhooks. Example: `https://example.com/webhooks/fintoc`. |
| `enabledEvents` | object | yes | Enabled webhook events array as JSON. Example: `account.refresh_intent.succeeded`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "enabled_events": {},
      "id": "string",
      "mode": "string",
      "name": "Ava Chen",
      "object": "string",
      "secret": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `description` | string |  |
| `enabled_events` | object |  |
| `id` | string |  |
| `mode` | string |  |
| `name` | string |  |
| `object` | string |  |
| `secret` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `POST /v1/webhook_endpoints` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-endpoint.md) for the provider-specific parameters and requirements.

