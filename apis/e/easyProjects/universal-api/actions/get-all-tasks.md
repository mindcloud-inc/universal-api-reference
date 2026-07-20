# Easy Projects: Get All Tasks

Retrieves tasks visible to the current Easy Projects user.

```
GET https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-all-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-all-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-all-tasks?${params}`, {
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
      "attachmentsCount": 1,
      "id": 1,
      "messagesCount": 1,
      "name": "Ava Chen",
      "priorityId": 1,
      "projectId": 1,
      "projectName": "Ava Chen",
      "statusId": 1,
      "taskTypeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentsCount` | number |  |
| `id` | number |  |
| `messagesCount` | number |  |
| `name` | string |  |
| `priorityId` | number |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `statusId` | number |  |
| `taskTypeId` | number |  |

## Native endpoint

Through the native Easy Projects API, this operation is `GET /api/v1/tasks` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-tasks.md) for the provider-specific parameters and requirements.

