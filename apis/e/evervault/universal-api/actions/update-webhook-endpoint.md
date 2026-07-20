# Evervault: Update Webhook Endpoint

Updates an existing webhook endpoint in Evervault.

```
PUT https://connect.mindcloud.co/v1/universal/evervault/latest/actions/update-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/update-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evervault/latest/actions/update-webhook-endpoint', {
  method: 'PUT',
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
      "createdAt": 1,
      "events": [
        "string"
      ],
      "id": "string",
      "updatedAt": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `events` | array<string> |  |
| `id` | string |  |
| `updatedAt` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Evervault API, this operation is `PATCH /webhook-endpoints/{webhook_endpoint_id}` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-endpoint.md) for the provider-specific parameters and requirements.

