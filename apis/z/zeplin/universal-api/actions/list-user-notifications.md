# Zeplin: List User Notifications

Retrieves a list of user notifications from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-user-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-user-notifications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-user-notifications?${params}`, {
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
| `isRead` | boolean | no | Whether the notification is read or not |
| `type[]` | array<string> | no | Filter by type Example: `?type=project.extension&type=styleguide.extension` |

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

Through the native Zeplin API, this operation is `GET /users/me/notifications` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-notifications.md) for the provider-specific parameters and requirements.

