# JoggAI: Create Webhook Endpoint



```
POST https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": [
    "string"
  ],
  "status": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-webhook-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": ["string"],
    "status": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[]` | array<string> | yes | Webhook event types to subscribe to. |
| `status` | string | yes | Initial webhook status: enabled or disabled. |
| `url` | string | yes | HTTPS endpoint that should receive webhook events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "endpointId": "string",
      "events": [
        "string"
      ],
      "secret": "string",
      "status": "string",
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `endpointId` | string |  |
| `events[]` | string |  |
| `secret` | string |  |
| `status` | string |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native JoggAI API, this operation is `POST /v2/endpoint` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-endpoint.md) for the provider-specific parameters and requirements.

