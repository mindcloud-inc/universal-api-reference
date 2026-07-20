# SWELLEnterprise: Update Webhook Subscription

Updates a webhook subscription in SWELLEnterprise.

```
PUT https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/update-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/update-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/update-webhook-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The webhook subscription ID. |
| `name` | string | no | The webhook name. |
| `url` | string | no | The webhook URL. |
| `events[]` | array<string> | no | Array of event types. |
| `isActive` | boolean | no | Whether the webhook is active. |
| `headers` | object | no | Custom headers. |
| `maxRetries` | number | no | Maximum retry attempts. |
| `timeout` | number | no | Request timeout. |

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
| `url` | string |  |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `PUT /webhooks/subscriptions/:id` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-subscription.md) for the provider-specific parameters and requirements.

