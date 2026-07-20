# Chainstream: Get Webhook Endpoint

Retrieves a webhook endpoint from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-webhook-endpoint?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-webhook-endpoint?${params}`, {
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
| `id` | string | yes | Webhook endpoint ID |

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

Through the native Chainstream API, this operation is `GET /v2/webhook/endpoint/:id` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-endpoint.md) for the provider-specific parameters and requirements.

