# CheckFlow: Add Task Assignees by Name



```
PUT https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/add-task-assignees-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/add-task-assignees-by-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "5678",
  "assigneeNames[]": "MindCloud Apps",
  "isAssignedExclusively": "false",
  "deleteExistingAssignees": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/add-task-assignees-by-name', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "5678",
    "assigneeNames[]": "MindCloud Apps",
    "isAssignedExclusively": "false",
    "deleteExistingAssignees": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | The ID of the task to update assignees for. Example: `5678`. |
| `assigneeNames[]` | array<string> | yes | The member or group names to assign to the task. Example: `MindCloud Apps`. |
| `isAssignedExclusively` | boolean | yes | Whether the named assignees should replace any other candidates for assignment selection. Example: `false`. |
| `deleteExistingAssignees` | boolean | yes | Whether existing assignees should be removed before adding the new names. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        {}
      ],
      "comments": [
        {}
      ],
      "fields": [
        {}
      ],
      "tags": [
        {}
      ],
      "taskCompletedByEmail": "ava@example.com",
      "taskCompletedByName": "Ava Chen",
      "taskCompletedDateTime": "2026-05-07T12:00:00.000Z",
      "taskDueDateTime": "2026-05-07T12:00:00.000Z",
      "taskId": 1,
      "taskIsComplete": true,
      "taskIsCurrentlyHalted": true,
      "taskIsCurrentlyHidden": true,
      "taskIsHeading": true,
      "taskIsNotApplicable": true,
      "taskKey": "string",
      "taskName": "Ava Chen",
      "taskNotApplicableByEmail": "ava@example.com",
      "taskNotApplicableByName": "Ava Chen",
      "taskNotApplicableDateTime": "2026-05-07T12:00:00.000Z",
      "taskUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> |  |
| `comments` | array<object> |  |
| `fields` | array<object> |  |
| `tags` | array<object> |  |
| `taskCompletedByEmail` | string |  |
| `taskCompletedByName` | string |  |
| `taskCompletedDateTime` | date |  |
| `taskDueDateTime` | date |  |
| `taskId` | number |  |
| `taskIsComplete` | boolean |  |
| `taskIsCurrentlyHalted` | boolean |  |
| `taskIsCurrentlyHidden` | boolean |  |
| `taskIsHeading` | boolean |  |
| `taskIsNotApplicable` | boolean |  |
| `taskKey` | string |  |
| `taskName` | string |  |
| `taskNotApplicableByEmail` | string |  |
| `taskNotApplicableByName` | string |  |
| `taskNotApplicableDateTime` | date |  |
| `taskUrl` | string |  |

## Native endpoint

Through the native CheckFlow API, this operation is `POST /api/task/assign-by-name` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-task-assignees-by-name.md) for the provider-specific parameters and requirements.

