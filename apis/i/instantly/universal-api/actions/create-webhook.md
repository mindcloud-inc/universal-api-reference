# Instantly: Create Webhook

Creates a new webhook in Instantly.

```
POST https://connect.mindcloud.co/v1/universal/instantly/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetHookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetHookUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetHookUrl` | string | yes | Target URL to send webhook payloads. |
| `name` | string | no | User-defined webhook name. |
| `eventType` | string | no | Event type to trigger the webhook, such as all_events or email_sent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_type": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": 1,
      "target_hook_url": "https://example.com",
      "timestamp_created": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_type` | string | Webhook event type. |
| `id` | string | Unique webhook identifier. |
| `name` | string | Webhook name. |
| `status` | number | Webhook status. |
| `target_hook_url` | string | Target webhook URL. |
| `timestamp_created` | date | Timestamp when the webhook was created. |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/webhooks` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

