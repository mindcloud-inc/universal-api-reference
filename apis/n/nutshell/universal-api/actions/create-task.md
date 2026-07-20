# Nutshell: Create Task

Creates a new task in Nutshell.

```
POST https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutshell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Title of the task. |
| `description` | string | no | Description of the task. |
| `dueTime` | date | no | Due time for the task. |
| `links.relatedEntity` | string | no | Entity ID to attach to the task. |
| `links.assignee` | string | no | User ID to assign to the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedTime": {},
      "createdTime": "2026-05-07T12:00:00.000Z",
      "creatorEntity": {},
      "deletedTime": {},
      "description": "string",
      "dueTime": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "htmlUrl": "https://example.com",
      "htmlUrlPath": "https://example.com",
      "id": "string",
      "isAiGenerated": true,
      "isCompleted": true,
      "isOverdue": true,
      "isRecurring": true,
      "links": {
        "assignee": "https://example.com",
        "completer": {},
        "creator": "https://example.com",
        "relatedEntity": "https://example.com"
      },
      "recurringPeriod": {},
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedTime` | object |  |
| `createdTime` | date |  |
| `creatorEntity` | object |  |
| `deletedTime` | object |  |
| `description` | string |  |
| `dueTime` | date |  |
| `href` | string |  |
| `htmlUrl` | string |  |
| `htmlUrlPath` | string |  |
| `id` | string |  |
| `isAiGenerated` | boolean |  |
| `isCompleted` | boolean |  |
| `isOverdue` | boolean |  |
| `isRecurring` | boolean |  |
| `links.assignee` | string |  |
| `links.completer` | object |  |
| `links.creator` | string |  |
| `links.relatedEntity` | string |  |
| `recurringPeriod` | object |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Nutshell API, this operation is `POST /tasks` (base URL `https://app.nutshell.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

