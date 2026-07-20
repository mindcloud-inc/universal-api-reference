# Zoho Connect: Create Task

Creates a new task in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "position": 1,
  "priority": "string",
  "scopeID": "string",
  "sectionId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "position": 1,
    "priority": "string",
    "scopeID": "string",
    "sectionId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | no | ID of the board to add the task to. |
| `checkList` | string | no | Checklist items for the task. |
| `dayOfMonth` | number | no | Monthly repeat day. |
| `dayOfWeek` | string | no | Weekly repeat days. Accepts multiple values in one string, delimited by `,`. |
| `desc` | string | no | Task description. |
| `edate` | number | no | Due date day. |
| `emonth` | number | no | Due date month. |
| `eyear` | number | no | Due date year. |
| `fileIds` | string | no | Comma-separated file IDs to attach to the task. Accepts multiple values in one string, delimited by `,`. |
| `howOftenRepetition` | number | no | How often the task repeats. Default: `1`. |
| `isSelfReminder` | boolean | no | Whether the task should include a reminder. Default: `false`. |
| `monthOfYear` | number | no | Month of the year for yearly recurring tasks. |
| `position` | number | yes | Board task position. |
| `priority` | string | yes | Priority level: None, Low, Medium, or High. |
| `remDay` | number | no | Task reminder day. |
| `remHour` | number | no | Task reminder hour in 24-hour format. |
| `remMin` | number | no | Task reminder minute. |
| `remMonth` | number | no | Task reminder month. |
| `remYear` | number | no | Task reminder year. |
| `repeatEndDate` | number | no | Day of month when task recurrence should end. |
| `repeatEndMonth` | number | no | Month when task recurrence should end. |
| `repeatEndYear` | number | no | Year when task recurrence should end. |
| `scopeID` | string | yes | ID of the network where the task is created. |
| `sectionId` | string | yes | Board section to place the task in. |
| `streamId` | string | no | Optional stream ID to link a task to a post. |
| `tagColors` | string | no | Colors for task tags. Accepts multiple values in one string, delimited by `,`. |
| `tagNames` | string | no | Hashtag names associated with the task. Accepts multiple values in one string, delimited by `,`. |
| `title` | string | yes | Task title. |
| `userIds` | string | no | Comma-separated user IDs to assign to the task. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTask": {
        "stream": {
          "id": "string",
          "status": "string",
          "task": {
            "canComplete": true,
            "canEdit": true,
            "desc": "string",
            "id": "string",
            "priority": "string",
            "status": 1,
            "taskPriority": {
              "name": "Ava Chen"
            },
            "taskStatus": {
              "name": "Ava Chen"
            },
            "title": "string"
          },
          "type": "string",
          "url": "https://example.com"
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
| `addTask.stream.id` | string |  |
| `addTask.stream.status` | string |  |
| `addTask.stream.task.canComplete` | boolean |  |
| `addTask.stream.task.canEdit` | boolean |  |
| `addTask.stream.task.desc` | string |  |
| `addTask.stream.task.id` | string |  |
| `addTask.stream.task.priority` | string |  |
| `addTask.stream.task.status` | number |  |
| `addTask.stream.task.taskPriority.name` | string |  |
| `addTask.stream.task.taskStatus.name` | string |  |
| `addTask.stream.task.title` | string |  |
| `addTask.stream.type` | string |  |
| `addTask.stream.url` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/addTask` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

