# Geral: Get Notification Handler

Retrieves a notification handler from Geral by ID.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-notification-handler
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-notification-handler?connectionId=$CONNECTION_ID&notificationHandlerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "notificationHandlerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-notification-handler?${params}`, {
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
| `notificationHandlerId` | number | yes | The notification handler ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_enabled": true,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "settings": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetime` | date | Creation timestamp. |
| `id` | number | Notification handler ID. |
| `is_enabled` | boolean | Whether the notification handler is enabled. |
| `last_datetime` | date | Last update timestamp. |
| `name` | string | Notification handler name. |
| `settings` | object | Notification handler settings. |
| `type` | string | Notification handler type. |

## Native endpoint

Through the native Geral API, this operation is `GET /notification-handlers/:notification_handler_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification-handler.md) for the provider-specific parameters and requirements.

