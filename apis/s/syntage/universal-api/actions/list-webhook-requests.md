# Syntage: List Webhook Requests

Retrieves webhook requests from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-webhook-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-webhook-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-webhook-requests?${params}`, {
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
      "@id": "string",
      "@type": "string",
      "createdAt": "string",
      "id": "string",
      "responseStatusCode": 1,
      "responseTime": 1,
      "updatedAt": "string",
      "url": "https://example.com",
      "webhookEndpoint": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@id` | string |  |
| `@type` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `responseStatusCode` | number |  |
| `responseTime` | number |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `webhookEndpoint` | object |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /webhook-requests` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-requests.md) for the provider-specific parameters and requirements.

