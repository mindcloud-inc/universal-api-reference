# Zeplin: Get User Notification

Retrieves an user notification from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-user-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-user-notification?connectionId=$CONNECTION_ID&notificationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "notificationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-user-notification?${params}`, {
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
| `notificationId` | string | yes | Notification id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "actor": {},
      "context": {},
      "id": "string",
      "is_read": true,
      "resource": {},
      "timestamp": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `actor` | object |  |
| `context` | object |  |
| `id` | string |  |
| `is_read` | boolean |  |
| `resource` | object |  |
| `timestamp` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /users/me/notifications/{notification_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-notification.md) for the provider-specific parameters and requirements.

