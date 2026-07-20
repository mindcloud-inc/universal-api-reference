# Agent Mail: Get Webhook

Retrieves a specific webhook from AgentMail.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | The AgentMail webhook ID. |

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

Through the native Agent Mail API, this operation is `GET /webhooks/{webhook_id}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

