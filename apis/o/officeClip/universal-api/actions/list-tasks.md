# OfficeClip: List Tasks

Retrieves tasks from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-tasks?${params}`, {
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
      "data": [
        {
          "dueDate": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "isComplete": true,
          "isPrivate": true,
          "security": {
            "append": true,
            "delete": true,
            "read": true,
            "write": true
          },
          "subject": "string",
          "taskPriorityName": "Ava Chen",
          "taskStatusCategory": "string",
          "taskStatusName": "Ava Chen"
        }
      ],
      "pagination": {
        "first": "string",
        "last": "string",
        "next": "string",
        "prev": "string",
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].dueDate` | date |  |
| `data[].id` | string |  |
| `data[].isComplete` | boolean |  |
| `data[].isPrivate` | boolean |  |
| `data[].security.append` | boolean |  |
| `data[].security.delete` | boolean |  |
| `data[].security.read` | boolean |  |
| `data[].security.write` | boolean |  |
| `data[].subject` | string |  |
| `data[].taskPriorityName` | string |  |
| `data[].taskStatusCategory` | string |  |
| `data[].taskStatusName` | string |  |
| `pagination.first` | string |  |
| `pagination.last` | string |  |
| `pagination.next` | string |  |
| `pagination.prev` | string |  |
| `pagination.total` | number |  |

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/task-summary` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

