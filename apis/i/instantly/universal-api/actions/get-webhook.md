# Instantly: Get Webhook

Retrieves a webhook from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-webhook?${params}`, {
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
| `id` | string | yes | Webhook UUID. |

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

Through the native Instantly API, this operation is `GET /api/v2/webhooks/:id` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

