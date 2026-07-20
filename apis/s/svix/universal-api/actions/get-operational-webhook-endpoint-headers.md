# Svix: Get Operational Webhook Endpoint Headers

Retrieves operational webhook endpoint headers from Svix.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-operational-webhook-endpoint-headers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-operational-webhook-endpoint-headers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-operational-webhook-endpoint-headers?${params}`, {
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
      "headers": {},
      "sensitive": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `headers` | object |  |
| `sensitive` | array<string> |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/operational-webhook/endpoint/{endpoint_id}/headers` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-operational-webhook-endpoint-headers.md) for the provider-specific parameters and requirements.

