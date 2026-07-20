# Calendly: Create Webhook Subscription

Creates a webhook subscription in Calendly.

```
POST https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/webhooks/calendly",
  "events[]": [
    "string"
  ],
  "organization": "https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e",
  "scope": "organization"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/webhooks/calendly",
    "events[]": ["string"],
    "organization": "https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e",
    "scope": "organization"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | HTTPS endpoint to receive webhook deliveries. Default: `https://example.com/webhooks/calendly`. |
| `events[]` | array<string> | yes | Webhook event list. |
| `organization` | string | yes | Organization URI for webhook scope. Default: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. |
| `scope` | string | yes | Subscription scope (organization or user). Default: `organization`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | string | no | User URI when using user scope. Default: `https://api.calendly.com/users/264e5a40-147f-45f9-a96c-a6f2f0a91dff`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Calendly API returns.

## Native endpoint

Through the native Calendly API, this operation is `POST /webhook_subscriptions` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-subscription.md) for the provider-specific parameters and requirements.

