# HyperDone: Create Task



```
POST https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HyperDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskName": "Weekly planning task"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperDone/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskName": "Weekly planning task"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskName` | string | yes | Required task name. Example: `Weekly planning task`. |
| `taskDescription` | string | no | Optional description for the task. Example: `Optional details about the task.`. |
| `columnId` | string | no | Optional target column ID from List Columns. Example: `Select a column when available.`. |
| `columnDate` | date | no | Optional target calendar date when creating on calendar boards. Example: `2026-04-11`. |
| `dueDate` | date | no | Optional due date for the task. Example: `2026-04-18`. |
| `tags[]` | array<string> | no | Optional array of tag IDs from List Tags. Accepts multiple values as an array. Example: `Select one or more tags.`. |
| `assignedTo[]` | array<string> | no | Optional array of board member IDs from List Board Members. Accepts multiple values as an array. Example: `Select one or more board members.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HyperDone API returns.

## Native endpoint

Through the native HyperDone API, this operation is `POST /AddTask` (base URL `https://hyperdone.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

