# Faraday: Create Webhook Endpoint

Creates a new webhook endpoint in Faraday.

```
POST https://connect.mindcloud.co/v1/universal/faraday/latest/actions/create-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faraday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/create-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/faraday/latest/actions/create-webhook-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "enabledEvents": [
        "string"
      ],
      "id": "string",
      "status": "string",
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
| `createdAt` | string | Creation timestamp. |
| `enabledEvents` | array<string> | Enabled Faraday webhook events. |
| `id` | string | Webhook endpoint ID. |
| `status` | string | Webhook endpoint status. |
| `updatedAt` | string | Last update timestamp. |
| `url` | string | Webhook destination URL. |

## Native endpoint

Through the native Faraday API, this operation is `POST /webhook_endpoints` (base URL `https://api.faraday.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-endpoint.md) for the provider-specific parameters and requirements.

