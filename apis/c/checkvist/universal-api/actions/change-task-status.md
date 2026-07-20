# Checkvist: Change Task Status

Updates a task status in Checkvist.

```
PUT https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/change-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/change-task-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "checklistId": 1,
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/change-task-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "checklistId": 1,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Use close, invalidate, or reopen. |
| `checklistId` | number | yes | The checklist ID. |
| `taskId` | number | yes | The task ID. |

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

Through the native Checkvist API, this operation is `POST /checklists/:checklistId/tasks/:taskId/:action.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-task-status.md) for the provider-specific parameters and requirements.

