# SuperOps IT: Get Task



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | The SuperOps task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "getTask": {
        "actualEndDate": "2026-05-07T12:00:00.000Z",
        "actualStartDate": "2026-05-07T12:00:00.000Z",
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
| `getTask.actualEndDate` | date |  |
| `getTask.actualStartDate` | date |  |
| `getTask.description` | string |  |
| `getTask.displayId` | string |  |
| `getTask.estimatedTime` | number |  |
| `getTask.overdue` | boolean |  |
| `getTask.status` | string |  |
| `getTask.taskId` | string |  |
| `getTask.taskOrder` | number |  |
| `getTask.techGroup.groupId` | string |  |
| `getTask.techGroup.name` | string |  |
| `getTask.technician.name` | string |  |
| `getTask.technician.userId` | string |  |
| `getTask.title` | string |  |
| `getTask.workItem.displayId` | string |  |
| `getTask.workItem.module` | string |  |
| `getTask.workItem.workId` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

