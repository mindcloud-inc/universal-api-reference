# Quiltt: Create Webhook Subscription



```
POST https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/create-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quiltt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventTypes": "string",
  "name": "Ava Chen",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventTypes": "string",
    "name": "Ava Chen",
    "targetUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventTypes` | list<string> | yes | List of webhook event types to subscribe to. Accepts multiple values as an array. |
| `name` | string | yes | Webhook subscription name. |
| `targetUrl` | string | yes | URL that receives webhook deliveries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "disabled": true,
      "eventTypes": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "targetUrl": "https://example.com",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `disabled` | boolean |  |
| `eventTypes` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `targetUrl` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Quiltt API, this operation is `POST /v1/webhooks/subscriptions` (base URL `https://api.quiltt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription.md) for the provider-specific parameters and requirements.

