# HelpSpace: Update Task

Updates an existing task in HelpSpace.

```
PUT https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | HelpSpace task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {},
      "attachments": [
        {}
      ],
      "attachmentsCount": 1,
      "board": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {},
      "customer": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "doneAt": "2026-05-07T12:00:00.000Z",
      "dueAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isArchived": true,
      "isOverdue": true,
      "number": "string",
      "priority": "string",
      "status": {},
      "subTasks": [
        {}
      ],
      "subtasksCountDone": 1,
      "subtasksCountTotal": 1,
      "tags": [
        {}
      ],
      "tickets": [
        {}
      ],
      "ticketsCount": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "watchers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | object |  |
| `attachments` | array<object> |  |
| `attachmentsCount` | number |  |
| `board` | object |  |
| `createdAt` | date |  |
| `creator` | object |  |
| `customer` | object |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `doneAt` | date |  |
| `dueAt` | date |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `isOverdue` | boolean |  |
| `number` | string |  |
| `priority` | string |  |
| `status` | object |  |
| `subTasks` | array<object> |  |
| `subtasksCountDone` | number |  |
| `subtasksCountTotal` | number |  |
| `tags` | array<object> |  |
| `tickets` | array<object> |  |
| `ticketsCount` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `watchers` | array<object> |  |

## Native endpoint

Through the native HelpSpace API, this operation is `PATCH /scrum/tasks/{id}` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

