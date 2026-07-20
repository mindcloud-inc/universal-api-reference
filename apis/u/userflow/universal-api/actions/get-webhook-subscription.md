# Userflow: Get Webhook Subscription

Retrieves a webhook subscription from Userflow by ID.

```
GET https://connect.mindcloud.co/v1/universal/userflow/latest/actions/get-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/get-webhook-subscription?connectionId=$CONNECTION_ID&webhookSubscriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookSubscriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/get-webhook-subscription?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookSubscriptionId` | string | yes | ID of the webhook subscription. |

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

Through the native Userflow API, this operation is `GET /webhook_subscriptions/:webhook_subscription_id` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-subscription.md) for the provider-specific parameters and requirements.

