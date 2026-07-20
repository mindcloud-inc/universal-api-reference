# Pledge: Get Webhook Endpoint

Retrieves a webhook endpoint from Pledge.

```
GET https://connect.mindcloud.co/v1/universal/pledge/latest/actions/get-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/get-webhook-endpoint?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pledge/latest/actions/get-webhook-endpoint?${params}`, {
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
| `id` | string | yes | Webhook endpoint ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Pledge API, this operation is `GET /webhooks/[:id]` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-endpoint.md) for the provider-specific parameters and requirements.

