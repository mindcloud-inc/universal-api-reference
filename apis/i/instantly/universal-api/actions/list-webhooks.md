# Instantly: List Webhooks

Retrieves webhooks from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Instantly API, this operation is `GET /api/v2/webhooks` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

