# Checkvist: Create Task

Creates a task in Checkvist.

```
POST https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checklistId": 1,
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checklistId": 1,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checklistId` | number | yes | The checklist ID. |
| `content` | string | yes | The task text. |
| `dueDate` | string | no | A due date in Checkvist smart syntax. |
| `parentId` | string | no | The parent task ID. |
| `position` | number | no | The 1-based position under the parent task. |
| `priority` | number | no | The task priority or color, from 0 to 9. |
| `status` | string | no | The optional task status. |
| `tags` | string | no | A comma-separated list of tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeIds": [
        1
      ],
      "backlinkIds": [
        1
      ],
      "checklistId": 1,
      "collapsed": true,
      "commentsCount": 1,
      "content": "string",
      "createdAt": "string",
      "details": {},
      "due": "string",
      "id": 1,
      "linkIds": [
        1
      ],
      "parentId": 1,
      "position": 1,
      "priority": 1,
      "status": 1,
      "tags": {},
      "tagsAsText": "string",
      "tasks": [
        1
      ],
      "updatedAt": "string",
      "updateLine": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeIds` | array<number> |  |
| `backlinkIds` | array<number> |  |
| `checklistId` | number |  |
| `collapsed` | boolean |  |
| `commentsCount` | number |  |
| `content` | string |  |
| `createdAt` | string |  |
| `details` | object |  |
| `due` | string |  |
| `id` | number |  |
| `linkIds` | array<number> |  |
| `parentId` | number |  |
| `position` | number |  |
| `priority` | number |  |
| `status` | number |  |
| `tags` | object |  |
| `tagsAsText` | string |  |
| `tasks` | array<number> |  |
| `updatedAt` | string |  |
| `updateLine` | string |  |

## Native endpoint

Through the native Checkvist API, this operation is `POST /checklists/:checklistId/tasks.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

