# Userflow: Update Webhook Subscription

Updates an existing webhook subscription in Userflow.

```
PUT https://connect.mindcloud.co/v1/universal/userflow/latest/actions/update-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/update-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookSubscriptionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userflow/latest/actions/update-webhook-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookSubscriptionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `disabled` | boolean | no | Whether the webhook subscription is disabled. |
| `topics[]` | array<string> | no | Updated webhook topics. |
| `url` | string | no | Updated webhook destination URL. |
| `webhookSubscriptionId` | string | yes | ID of the webhook subscription to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_version": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "disabled": true,
      "id": "string",
      "object": "string",
      "secret": "string",
      "topics": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_version` | string | API version used for the subscription. |
| `created_at` | date | Subscription creation timestamp. |
| `disabled` | boolean | Whether the subscription is disabled. |
| `id` | string | Webhook subscription ID. |
| `object` | string | Returned object type. |
| `secret` | string | Webhook secret when available. |
| `topics` | array<string> | Subscribed webhook topics. |
| `url` | string | Destination URL. |

## Native endpoint

Through the native Userflow API, this operation is `PATCH /webhook_subscriptions/:webhook_subscription_id` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-subscription.md) for the provider-specific parameters and requirements.

