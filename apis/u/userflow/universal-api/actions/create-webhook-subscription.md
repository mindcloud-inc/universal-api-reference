# Userflow: Create Webhook Subscription

Creates a webhook subscription in Userflow.

```
POST https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topics[]": [
    "string"
  ],
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topics[]": ["string"],
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiVersion` | string | no | API version to use for webhook payloads. |
| `topics[]` | array<string> | yes | Webhook topics to subscribe to. |
| `url` | string | yes | Webhook destination URL. |

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
| `secret` | string | Webhook secret. |
| `topics` | array<string> | Subscribed webhook topics. |
| `url` | string | Destination URL. |

## Native endpoint

Through the native Userflow API, this operation is `POST /webhook_subscriptions` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription.md) for the provider-specific parameters and requirements.

