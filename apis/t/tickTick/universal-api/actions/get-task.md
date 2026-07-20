# TickTick: Get Task

Retrieves a task from TickTick by project and task ID.

```
GET https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TickTick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/get-task?connectionId=$CONNECTION_ID&projectId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/get-task?${params}`, {
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
| `projectId` | list<string> | yes | Project identifier |
| `taskId` | string | yes | Task identifier |

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

Through the native TickTick API, this operation is `GET /open/v1/project/:projectId/task/:taskId` (base URL `https://api.ticktick.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

