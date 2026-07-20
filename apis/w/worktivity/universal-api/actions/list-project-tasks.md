# Worktivity: List Project Tasks

Retrieves project tasks from Worktivity with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-project-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-project-tasks?${params}`, {
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
      "assignees": [
        {}
      ],
      "createDate": "2026-05-07T12:00:00.000Z",
      "details": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "nonBillable": true,
      "priority": 1,
      "projectId": "string",
      "source": 1,
      "status": 1,
      "title": "string",
      "updateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> |  |
| `createDate` | date |  |
| `details` | string |  |
| `dueDate` | date |  |
| `id` | string |  |
| `nonBillable` | boolean |  |
| `priority` | number |  |
| `projectId` | string |  |
| `source` | number |  |
| `status` | number |  |
| `title` | string |  |
| `updateDate` | date |  |

## Native endpoint

Through the native Worktivity API, this operation is `POST /Project/ListTasks` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-tasks.md) for the provider-specific parameters and requirements.

