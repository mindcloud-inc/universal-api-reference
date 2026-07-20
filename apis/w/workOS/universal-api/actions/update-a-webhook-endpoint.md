# WorkOS: Update a Webhook Endpoint

Updates a webhook endpoint in your WorkOS environment.

```
PUT https://connect.mindcloud.co/v1/universal/workOS/latest/actions/update-a-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/update-a-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/update-a-webhook-endpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the Webhook Endpoint. |
| `endpoint_url` | string | no | The HTTPS URL where webhooks will be sent. |
| `status` | string | no | Whether the Webhook Endpoint is enabled or disabled. |
| `events` | list<string> | no | The events that the Webhook Endpoint is subscribed to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "endpoint_url": "https://example.com",
      "events": [
        "string"
      ],
      "id": "string",
      "message": "string",
      "object": "string",
      "secret": "string",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | An ISO 8601 timestamp. |
| `endpoint_url` | string | The URL to which webhooks are sent. |
| `events` | array<string> | The events that the Webhook Endpoint is subscribed to. |
| `id` | string | Unique identifier of the Webhook Endpoint. |
| `message` | string | WorkOS response field message. |
| `object` | string | Distinguishes the Webhook Endpoint object. |
| `secret` | string | The secret used to sign webhook payloads. |
| `status` | string | Whether the Webhook Endpoint is enabled or disabled. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `PATCH /webhook_endpoints/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-webhook-endpoint.md) for the provider-specific parameters and requirements.

