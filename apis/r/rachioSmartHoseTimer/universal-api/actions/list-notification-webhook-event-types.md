# Rachio Smart Hose Timer: List Notification Webhook Event Types

Retrieves notification webhook event types from Rachio.

```
GET https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-notification-webhook-event-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-notification-webhook-event-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/list-notification-webhook-event-types?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Notification webhook event type id. |
| `name` | string | Notification webhook event type name. |
| `type` | string | Notification webhook category. |

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `GET /public/notification/webhook_event_type` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notification-webhook-event-types.md) for the provider-specific parameters and requirements.

