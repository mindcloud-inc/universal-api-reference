# Redbooth: List Tasks

Retrieves tasks from Redbooth.

```
GET https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/list-tasks?${params}`, {
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
      "assigned_user_ids": [
        1
      ],
      "comments_count": 1,
      "id": 1,
      "name": "Ava Chen",
      "project_id": 1,
      "status": "string",
      "task_list_id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigned_user_ids` | array<number> |  |
| `comments_count` | number |  |
| `id` | number |  |
| `name` | string |  |
| `project_id` | number |  |
| `status` | string |  |
| `task_list_id` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Redbooth API, this operation is `GET /tasks` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

