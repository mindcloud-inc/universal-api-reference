# Ablefy: Update Webhook Endpoint

Updates an existing webhook endpoint in Ablefy.

```
PUT https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/update-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ablefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/update-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/update-webhook-endpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Webhook endpoint ID. |
| `name` | string | yes |  |
| `url` | string | yes |  |
| `eventForm` | string | no |  |
| `eventIds[]` | array<string> | no |  |
| `requestFormat` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ablefy API returns.

## Native endpoint

Through the native Ablefy API, this operation is `PUT /api/webhook_endpoints/:id` (base URL `https://api.myablefy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-endpoint.md) for the provider-specific parameters and requirements.

