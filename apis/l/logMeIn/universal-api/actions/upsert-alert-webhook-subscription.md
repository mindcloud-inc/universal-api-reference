# LogMeIn: Upsert Alert Webhook Subscription

Creates or updates an alert webhook subscription in LogMeIn.

```
PUT https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/upsert-alert-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/upsert-alert-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string",
  "channelData.url": "https://example.com",
  "channelData.sharedSecret": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/upsert-alert-webhook-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string",
    "channelData.url": "https://example.com",
    "channelData.sharedSecret": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionId` | string | yes | Required alert subscription ID scoped to the company and user. |
| `channelData.url` | string | yes | Webhook target URL for alert deliveries. |
| `channelData.sharedSecret` | string | yes | Shared secret used by the webhook receiver. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "subscriptionId": "string",
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
| `status` | string |  |
| `subscriptionId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `PUT /goto-resolve-alerts/v1/subscriptions/:subscriptionId` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-alert-webhook-subscription.md) for the provider-specific parameters and requirements.

