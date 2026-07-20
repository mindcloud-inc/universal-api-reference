# Fintoc: Update Webhook Endpoint

Updates a webhook endpoint in Fintoc.

```
PUT https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/update-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/update-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "whep_..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/update-webhook-endpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "whep_..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Webhook endpoint identifier. Example: `whep_...`. |

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

Through the native Fintoc API, this operation is `PATCH /v1/webhook_endpoints/:id` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-endpoint.md) for the provider-specific parameters and requirements.

