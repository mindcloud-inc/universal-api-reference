# TMetric: Patch Task



```
PUT https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/patch-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/patch-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/patch-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Workspace identifier. |
| `assignee.id` | number | no | Assignee identifier. |
| `description` | string | no | Updated task description. |
| `dueDate` | date | no | Task due date. |
| `estimatedMinutes` | number | no | Estimated time in minutes. |
| `isCompleted` | boolean | no | Whether the task is completed. |
| `name` | string | no | Updated task name. |
| `project.id` | number | no | Project identifier. |
| `taskId` | number | yes | Task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changes": [
        {
          "newValue": "string",
          "oldValue": "string",
          "text": "string",
          "timestamp": "2026-05-07T12:00:00.000Z",
          "type": "string",
          "user": {
            "iconUrl": "https://example.com",
            "id": 1,
            "name": "Ava Chen"
          }
        }
      ],
      "data": {
        "created": "2026-05-07T12:00:00.000Z",
        "creator": {
          "iconUrl": "https://example.com",
          "id": 1,
          "name": "Ava Chen"
        },
        "dueDate": "string",
        "estimatedMinutes": "string",
        "id": 1,
        "isCompleted": true,
        "modified": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "project": {
          "iconUrl": "https://example.com",
          "id": 1,
          "invoiceMethod": "string",
          "isBillable": true,
          "name": "Ava Chen",
          "status": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changes[].newValue` | string |  |
| `changes[].oldValue` | string |  |
| `changes[].text` | string |  |
| `changes[].timestamp` | date |  |
| `changes[].type` | string |  |
| `changes[].user.iconUrl` | string |  |
| `changes[].user.id` | number |  |
| `changes[].user.name` | string |  |
| `data.created` | date |  |
| `data.creator.iconUrl` | string |  |
| `data.creator.id` | number |  |
| `data.creator.name` | string |  |
| `data.dueDate` | string |  |
| `data.estimatedMinutes` | string |  |
| `data.id` | number |  |
| `data.isCompleted` | boolean |  |
| `data.modified` | date |  |
| `data.name` | string |  |
| `data.project.iconUrl` | string |  |
| `data.project.id` | number |  |
| `data.project.invoiceMethod` | string |  |
| `data.project.isBillable` | boolean |  |
| `data.project.name` | string |  |
| `data.project.status` | string |  |

## Native endpoint

Through the native TMetric API, this operation is `PATCH /accounts/:accountId/tasks/:taskId` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-task.md) for the provider-specific parameters and requirements.

