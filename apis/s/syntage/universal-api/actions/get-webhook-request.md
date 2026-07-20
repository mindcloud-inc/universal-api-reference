# Syntage: Get Webhook Request

Retrieves a webhook request from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-webhook-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-webhook-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-webhook-request?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The webhook request identifier. |

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

Through the native Syntage API, this operation is `GET /webhook-requests/:id` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-request.md) for the provider-specific parameters and requirements.

