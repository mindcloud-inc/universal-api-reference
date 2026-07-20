# SuperOps IT: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-tasks?${params}`, {
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
      "getTaskList": {
        "listInfo": {
          "page": 1,
          "pageSize": 1,
          "totalCount": 1
        },
        "tasks": [
          {
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
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getTaskList.listInfo.page` | number |  |
| `getTaskList.listInfo.pageSize` | number |  |
| `getTaskList.listInfo.totalCount` | number |  |
| `getTaskList.tasks[].displayId` | string |  |
| `getTaskList.tasks[].estimatedTime` | number |  |
| `getTaskList.tasks[].overdue` | boolean |  |
| `getTaskList.tasks[].status` | string |  |
| `getTaskList.tasks[].taskId` | string |  |
| `getTaskList.tasks[].taskOrder` | number |  |
| `getTaskList.tasks[].techGroup.groupId` | string |  |
| `getTaskList.tasks[].techGroup.name` | string |  |
| `getTaskList.tasks[].technician.name` | string |  |
| `getTaskList.tasks[].technician.userId` | string |  |
| `getTaskList.tasks[].title` | string |  |
| `getTaskList.tasks[].workItem.displayId` | string |  |
| `getTaskList.tasks[].workItem.module` | string |  |
| `getTaskList.tasks[].workItem.workId` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

