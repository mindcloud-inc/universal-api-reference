# SmartRoutes: List Notification Tasks



```
GET https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-notification-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-notification-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-notification-tasks?${params}`, {
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
| `updatedAtMin` | date | no | Only return notification tasks updated on or after this timestamp. |
| `status` | string | no | Filter notification tasks by status. |
| `type` | string | no | Filter notification tasks by type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "message": "string",
      "order": {},
      "scheduled_date": "string",
      "sent_date": "string",
      "status": "string",
      "subject": "string",
      "template": {},
      "to": "string",
      "visit": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `message` | string |  |
| `order` | object |  |
| `scheduled_date` | string |  |
| `sent_date` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `template` | object |  |
| `to` | string |  |
| `visit` | object |  |

## Native endpoint

Through the native SmartRoutes API, this operation is `GET /notification-tasks` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notification-tasks.md) for the provider-specific parameters and requirements.

