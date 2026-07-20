# Trackabi: List Task Subtasks

Retrieves subtasks for a task from Trackabi.

```
GET https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-task-subtasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-task-subtasks?connectionId=$CONNECTION_ID&limit=25&offset=0&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-task-subtasks?${params}`, {
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
| `taskId` | number | yes | The unique ID of the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "description": "string",
          "endDate": "string",
          "estimatedTime": "string",
          "id": 1,
          "name": "Ava Chen",
          "notBillable": "string",
          "parentTaskId": 1,
          "projectId": 1,
          "startDate": "string",
          "subtasksCount": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].description` | string |  |
| `[].endDate` | string |  |
| `[].estimatedTime` | string |  |
| `[].id` | number |  |
| `[].name` | string |  |
| `[].notBillable` | string |  |
| `[].parentTaskId` | number |  |
| `[].projectId` | number |  |
| `[].startDate` | string |  |
| `[].subtasksCount` | number |  |

## Native endpoint

Through the native Trackabi API, this operation is `GET /api/v1/tasks/:taskId/subtasks` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-task-subtasks.md) for the provider-specific parameters and requirements.

