# SuperOps IT: Create Task



```
POST https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The task title. |
| `status` | string | yes | The task status name. |
| `description` | string | no | Optional task description. |
| `estimatedTime` | number | no | Optional estimated time in minutes. |
| `scheduledStartDate` | date | no | Optional scheduled start datetime in ISO 8601 format. |
| `dueDate` | date | no | Optional due datetime in ISO 8601 format. |
| `technicianUserId` | string | no | Optional technician user ID. |
| `taskOrder` | number | no | Optional task order integer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTask": {
        "description": "string",
        "displayId": "string",
        "estimatedTime": 1,
        "overdue": true,
        "status": "string",
        "taskId": "string",
        "taskOrder": 1,
        "techGroup": {
          "groupId": "string",
          "name": "Ava Chen"
        },
        "technician": {
          "name": "Ava Chen",
          "userId": "string"
        },
        "title": "string",
        "workItem": {
          "displayId": "string",
          "module": "string",
          "workId": "string"
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
| `createTask.description` | string |  |
| `createTask.displayId` | string |  |
| `createTask.estimatedTime` | number |  |
| `createTask.overdue` | boolean |  |
| `createTask.status` | string |  |
| `createTask.taskId` | string |  |
| `createTask.taskOrder` | number |  |
| `createTask.techGroup.groupId` | string |  |
| `createTask.techGroup.name` | string |  |
| `createTask.technician.name` | string |  |
| `createTask.technician.userId` | string |  |
| `createTask.title` | string |  |
| `createTask.workItem.displayId` | string |  |
| `createTask.workItem.module` | string |  |
| `createTask.workItem.workId` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

