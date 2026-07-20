# Agent Mail: Create Webhook

Creates a new webhook in AgentMail.

```
POST https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventTypes[]": [
    "string"
  ],
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventTypes[]": ["string"],
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | no | Client-provided idempotency ID. |
| `eventTypes[]` | array<string> | yes | Webhook event types to subscribe to. Accepts multiple values as an array. |
| `inboxIds[]` | array<string> | no | Inbox IDs to subscribe to the webhook. Accepts multiple values as an array. |
| `podIds[]` | array<string> | no | Pod IDs to subscribe to the webhook. Accepts multiple values as an array. |
| `url` | string | yes | Webhook destination URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "event_types": [
        "string"
      ],
      "inbox_ids": [
        "string"
      ],
      "pod_ids": [
        "string"
      ],
      "secret": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "webhook_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | string | Client ID of the webhook. |
| `created_at` | date | Creation timestamp. |
| `enabled` | boolean | Whether the webhook is enabled. |
| `event_types` | array<string> | Webhook event types. |
| `inbox_ids` | array<string> | Scoped inbox IDs. |
| `pod_ids` | array<string> | Scoped pod IDs. |
| `secret` | string | Webhook signature secret. |
| `updated_at` | date | Last update timestamp. |
| `url` | string | Webhook endpoint URL. |
| `webhook_id` | string | ID of the webhook. |

## Native endpoint

Through the native Agent Mail API, this operation is `POST /webhooks` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

