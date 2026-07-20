# HelpSpace: List Tasks

Retrieves tasks from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-tasks?${params}`, {
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

Through the native HelpSpace API, this operation is `GET /scrum/tasks` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

