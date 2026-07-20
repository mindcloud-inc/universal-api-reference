# Float: List Project Tasks

Retrieves project tasks from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/list-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-project-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/list-project-tasks?${params}`, {
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
      "billable": 1,
      "budget": {},
      "countLoggedTime": 1,
      "countTasks": 1,
      "created": "string",
      "modified": "string",
      "phaseId": 1,
      "projectId": 1,
      "taskMetaId": 1,
      "taskName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | number |  |
| `budget` | object |  |
| `countLoggedTime` | number |  |
| `countTasks` | number |  |
| `created` | string |  |
| `modified` | string |  |
| `phaseId` | number |  |
| `projectId` | number |  |
| `taskMetaId` | number |  |
| `taskName` | string |  |

## Native endpoint

Through the native Float API, this operation is `GET /project-tasks` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-tasks.md) for the provider-specific parameters and requirements.

