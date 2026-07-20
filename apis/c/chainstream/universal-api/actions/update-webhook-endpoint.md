# Chainstream: Update Webhook Endpoint

Updates a webhook endpoint in Chainstream.

```
PUT https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/update-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/update-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpointId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/update-webhook-endpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpointId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpointId` | string | yes | Endpoint ID |
| `url` | string | no | Webhook destination URL |
| `channels[]` | array<string> | no | Webhook event channels to subscribe to |
| `description` | string | no | Endpoint description |
| `disabled` | boolean | no | Whether the endpoint is disabled |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Event filter configuration |
| `filterTypes[]` | array<string> | no | Event type filters |
| `metadata` | object | no | Endpoint metadata |
| `rateLimit` | number | no | Rate limit for the endpoint |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        [
          "string"
        ]
      ],
      "createdAt": "string",
      "description": "string",
      "disabled": true,
      "id": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels[]` | array<string> |  |
| `createdAt` | string |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `id` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `PATCH /v2/webhook/endpoint` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-endpoint.md) for the provider-specific parameters and requirements.

