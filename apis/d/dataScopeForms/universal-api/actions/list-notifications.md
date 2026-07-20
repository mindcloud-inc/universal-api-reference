# DataScope Forms: List Notifications

Retrieves notifications from DataScope Forms.

```
GET https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-notifications?${params}`, {
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
| `end` | string | no | End of the date range to fetch notifications for. |
| `start` | string | no | Start of the date range to fetch notifications for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "form_code": "string",
      "form_name": "Ava Chen",
      "id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Date when the notification was created. |
| `form_code` | string | Code of the form. |
| `form_name` | string | Name of the form. |
| `id` | string | Identifier of the notification. |
| `type` | string | Type of notification, such as PDF or Excel. |
| `updated_at` | date | Date when the notification was updated. |
| `url` | string | URL of the notified file. |
| `user` | string | Name or identifier of the user. |

## Native endpoint

Through the native DataScope Forms API, this operation is `GET /external/notifications` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notifications.md) for the provider-specific parameters and requirements.

