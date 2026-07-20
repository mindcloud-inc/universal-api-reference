# CheckFlow: List Task Assignments



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-task-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-task-assignments?connectionId=$CONNECTION_ID&assigneeId=21831&assigneeType=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assigneeId": "21831",
  "assigneeType": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-task-assignments?${params}`, {
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
| `assigneeId` | number | yes | The assignee ID to list assignments for. Example: `21831`. |
| `assigneeType` | number | yes | The assignee type. Use 1 for member and 2 for group. Example: `1`. |
| `includeTeamMemberGroups` | boolean | no | Whether to include tasks assigned via groups the member belongs to. Example: `true`. |
| `includeCompletedTasks` | boolean | no | Whether to include completed tasks in the results. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        {}
      ],
      "isAssignedExclusively": true,
      "taskId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> |  |
| `isAssignedExclusively` | boolean |  |
| `taskId` | number |  |

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/task/assignments` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-assignments.md) for the provider-specific parameters and requirements.

