# DataForB2B: Create Webhook Subscription

Creates a webhook subscription in DataForB2B.

```
POST https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/create-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/dataforb2b-webhook",
  "eventTypes": [
    "company_changed",
    "position_changed"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/dataforb2b-webhook",
    "eventTypes": ["company_changed","position_changed"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | HTTPS endpoint that should receive webhook deliveries. Default: `https://example.com/dataforb2b-webhook`. |
| `eventTypes` | object<string> | yes | List of event types to subscribe to. Default: `["company_changed","position_changed"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created_at": "string",
      "event_types": [
        "string"
      ],
      "id": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created_at` | string |  |
| `event_types` | array<string> |  |
| `id` | number |  |
| `url` | string |  |

## Native endpoint

Through the native DataForB2B API, this operation is `POST /webhooks` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription.md) for the provider-specific parameters and requirements.

