# Understory: Update Webhook Subscription

Updates an existing webhook subscription in Understory.

```
PUT https://connect.mindcloud.co/v1/universal/understory/latest/actions/update-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/understory/latest/actions/update-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string",
  "url": "https://example.com",
  "eventTypes[]": [
    "string"
  ],
  "state": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/understory/latest/actions/update-webhook-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string",
    "url": "https://example.com",
    "eventTypes[]": ["string"],
    "state": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionId` | string | yes | The unique identifier of the subscription. |
| `url` | string | yes | The URL to send webhook events to. |
| `eventTypes[]` | array<string> | yes | One or more event types to subscribe to. |
| `state` | list | yes | The state of the subscription. One of: `0`, `1`. |
| `metadata` | object | no | Optional custom metadata object for the subscription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "event_types": [
        [
          "string"
        ]
      ],
      "id": "string",
      "state": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `event_types[]` | array<string> |  |
| `id` | string |  |
| `state` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Understory API, this operation is `PUT /v1/webhook-subscriptions/{{subscriptionId}}` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-subscription.md) for the provider-specific parameters and requirements.

