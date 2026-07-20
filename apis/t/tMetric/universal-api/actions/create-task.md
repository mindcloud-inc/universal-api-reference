# TMetric: Create Task



```
POST https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1
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
| `dryRun` | boolean | no | Validate the task payload without saving. |
| `dueDate` | date | no | Task due date. |
| `estimatedMinutes` | number | no | Estimated time in minutes. |
| `isCompleted` | boolean | no | Whether the task is completed. |
| `name` | string | no | Task name. |
| `project.id` | number | no | Project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "creator": {
        "iconUrl": "https://example.com",
        "id": 1
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `creator.iconUrl` | string |  |
| `creator.id` | number |  |
| `dueDate` | string |  |
| `estimatedMinutes` | string |  |
| `id` | number |  |
| `isCompleted` | boolean |  |
| `modified` | date |  |
| `name` | string |  |
| `project.iconUrl` | string |  |
| `project.id` | number |  |
| `project.invoiceMethod` | string |  |
| `project.isBillable` | boolean |  |
| `project.name` | string |  |
| `project.status` | string |  |

## Native endpoint

Through the native TMetric API, this operation is `POST /accounts/:accountId/tasks` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

