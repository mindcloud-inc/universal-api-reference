# Chainstream: Create Webhook Endpoint

Creates a webhook endpoint in Chainstream.

```
POST https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/create-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/create-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/create-webhook-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Webhook destination URL |
| `channels[]` | array<string> | no | Webhook event channels to subscribe to |
| `description` | string | no | Endpoint description |
| `disabled` | boolean | no | Whether the endpoint is disabled |
| `filter` | string | no | Event filter configuration |
| `filterTypes[]` | array<string> | no | Event type filters |
| `metadata` | object | no | Endpoint metadata |
| `rateLimit` | number | no | Rate limit for the endpoint |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `secret` | string | no | Endpoint signing secret |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "disabled": true,
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels[]` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `id` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `POST /v2/webhook/endpoint` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-endpoint.md) for the provider-specific parameters and requirements.

