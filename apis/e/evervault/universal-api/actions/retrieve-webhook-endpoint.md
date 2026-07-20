# Evervault: Retrieve Webhook Endpoint

Retrieves a webhook endpoint from Evervault.

```
GET https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-webhook-endpoint?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-webhook-endpoint?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Evervault API, this operation is `GET /webhook-endpoints/{webhook_endpoint_id}` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-webhook-endpoint.md) for the provider-specific parameters and requirements.

