# 5pm: List Tasks

Retrieves tasks from 5pm.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/list-tasks?${params}`, {
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
      "count": 1,
      "items": [
        {
          "id": "string",
          "name": "Ava Chen",
          "ownerId": 1,
          "priority": 1,
          "progress": 1,
          "projectId": 1,
          "status": 1
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of tasks in this page. |
| `items[].id` | string | Task identifier. |
| `items[].name` | string | Task name. |
| `items[].ownerId` | number | Task owner user ID. |
| `items[].priority` | number | Task priority ID. |
| `items[].progress` | number | Task progress percentage. |
| `items[].projectId` | number | Parent project ID. |
| `items[].status` | number | Task status ID. |
| `total` | number | Total number of tasks available. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/tasks/getList` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

