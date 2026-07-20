# Svix: Get Operational Webhook Endpoint

Retrieves an operational webhook endpoint from Svix.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-operational-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-operational-webhook-endpoint?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-operational-webhook-endpoint?${params}`, {
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
      "createdAt": "string",
      "description": "string",
      "disabled": true,
      "filterTypes": [
        "string"
      ],
      "id": "string",
      "metadata": {},
      "rateLimit": 1,
      "uid": "string",
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
| `createdAt` | string |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `filterTypes` | array<string> |  |
| `id` | string |  |
| `metadata` | object |  |
| `rateLimit` | number |  |
| `uid` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/operational-webhook/endpoint/{endpoint_id}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-operational-webhook-endpoint.md) for the provider-specific parameters and requirements.

