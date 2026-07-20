# KanbanFlow: Get tasks by column

Retrieves tasks from a KanbanFlow column.

```
GET https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-tasks-by-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KanbanFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-tasks-by-column?connectionId=$CONNECTION_ID&columnId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "columnId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-tasks-by-column?${params}`, {
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
| `columnId` | string | yes | The KanbanFlow column ID to list tasks from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnId": "string",
      "columnName": "Ava Chen",
      "tasks": [
        {
          "collaborators": [
            {
              "userId": "string"
            }
          ],
          "color": "string",
          "columnId": "string",
          "description": "string",
          "labels": [
            {
              "name": "Ava Chen",
              "pinned": true
            }
          ],
          "name": "Ava Chen",
          "subTasks": [
            {
              "finished": true,
              "name": "Ava Chen"
            }
          ],
          "totalSecondsEstimate": 1,
          "totalSecondsSpent": 1
        }
      ],
      "tasksLimited": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnId` | string |  |
| `columnName` | string |  |
| `tasks` | array<object> |  |
| `tasks[].collaborators` | array<object> |  |
| `tasks[].collaborators[].userId` | string |  |
| `tasks[].color` | string |  |
| `tasks[].columnId` | string |  |
| `tasks[].description` | string |  |
| `tasks[].labels` | array<object> |  |
| `tasks[].labels[].name` | string |  |
| `tasks[].labels[].pinned` | boolean |  |
| `tasks[].name` | string |  |
| `tasks[].subTasks` | array<object> |  |
| `tasks[].subTasks[].finished` | boolean |  |
| `tasks[].subTasks[].name` | string |  |
| `tasks[].totalSecondsEstimate` | number |  |
| `tasks[].totalSecondsSpent` | number |  |
| `tasksLimited` | boolean |  |

## Native endpoint

Through the native KanbanFlow API, this operation is `GET /tasks` (base URL `https://kanbanflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tasks-by-column.md) for the provider-specific parameters and requirements.

