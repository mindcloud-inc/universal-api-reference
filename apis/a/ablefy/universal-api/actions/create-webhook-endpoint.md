# Ablefy: Create Webhook Endpoint

Creates a new webhook endpoint in Ablefy.

```
POST https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ablefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-webhook-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `name` | string | yes |  |
| `url` | string | yes |  |
| `eventForm` | list<string> | no | One of: `all_events`, `selected_events`. |
| `eventIds[]` | array<string> | no |  |
| `requestFormat` | list<string> | no | One of: `json`, `x_www_form_urlencoded`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ablefy API returns.

## Native endpoint

Through the native Ablefy API, this operation is `POST /api/webhook_endpoints` (base URL `https://api.myablefy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-endpoint.md) for the provider-specific parameters and requirements.

