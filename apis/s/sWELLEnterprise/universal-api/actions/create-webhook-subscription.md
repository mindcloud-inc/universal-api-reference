# SWELLEnterprise: Create Webhook Subscription

Creates a webhook subscription in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com",
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com",
    "events[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The webhook name. |
| `url` | string | yes | The webhook URL. |
| `events[]` | array<string> | yes | Array of event types. |
| `headers` | object | no | Custom headers to send. |
| `maxRetries` | number | no | Maximum retry attempts. |
| `timeout` | number | no | Request timeout in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        "string"
      ],
      "id": 1,
      "is_active": true,
      "name": "Ava Chen",
      "secret": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[]` | string |  |
| `id` | number |  |
| `is_active` | boolean |  |
| `name` | string |  |
| `secret` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /webhooks/subscriptions` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription.md) for the provider-specific parameters and requirements.

