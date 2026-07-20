# Fintoc: List Webhook Endpoints

Retrieves webhook endpoints from Fintoc.

```
GET https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-webhook-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-webhook-endpoints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-webhook-endpoints?${params}`, {
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

Through the native Fintoc API, this operation is `GET /v1/webhook_endpoints` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-endpoints.md) for the provider-specific parameters and requirements.

