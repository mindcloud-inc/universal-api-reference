# TickTick: Update Task

Updates an existing task in TickTick.

```
PUT https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TickTick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "id": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "id": "string",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Task identifier |
| `id` | string | yes | Task ID in request body |
| `projectId` | list<string> | yes | Project identifier |
| `title` | string | no | Task title |
| `content` | string | no | Task content |
| `desc` | string | no | Task description |
| `isAllDay` | boolean | no | Whether task is all day |
| `startDate` | string | no | Task start date time |
| `dueDate` | string | no | Task due date time |
| `timeZone` | string | no | Task time zone |
| `priority` | number | no | Task priority |
| `reminders[]` | array<string> | no | List of reminder triggers |
| `repeatFlag` | string | no | Recurring rules of task |
| `sortOrder` | number | no | Task order |
| `items[]` | array<object> | no | List of subtasks |
| `items[].title` | string | no | Subtask title |
| `items[].startDate` | date | no | Subtask start date/time |
| `items[].isAllDay` | boolean | no | Whether subtask is all day |
| `items[].sortOrder` | number | no | Subtask order |
| `items[].timeZone` | string | no | Subtask time zone |
| `items[].status` | number | no | Subtask completion status |
| `items[].completedTime` | date | no | Subtask completed time |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedTime": "string",
      "content": "string",
      "desc": "string",
      "dueDate": "string",
      "id": "string",
      "isAllDay": true,
      "items": [
        {}
      ],
      "kind": "string",
      "priority": 1,
      "projectId": "string",
      "reminders": [
        "string"
      ],
      "repeatFlag": "string",
      "sortOrder": 1,
      "startDate": "string",
      "status": 1,
      "timeZone": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedTime` | string |  |
| `content` | string |  |
| `desc` | string |  |
| `dueDate` | string |  |
| `id` | string |  |
| `isAllDay` | boolean |  |
| `items` | array<object> |  |
| `kind` | string |  |
| `priority` | number |  |
| `projectId` | string |  |
| `reminders` | array<string> |  |
| `repeatFlag` | string |  |
| `sortOrder` | number |  |
| `startDate` | string |  |
| `status` | number |  |
| `timeZone` | string |  |
| `title` | string |  |

## Native endpoint

Through the native TickTick API, this operation is `POST /open/v1/task/:taskId` (base URL `https://api.ticktick.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

