# CheckFlow: List Tasks by Task Key



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-tasks-by-task-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-tasks-by-task-key?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-tasks-by-task-key?${params}`, {
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
| `taskKey` | string | no | The key of the task to match. Example: `07072bc4-f1eb-4536-819a-1ddb7dc109a1`. |
| `status` | string | no | Task status filter. Example: `ALL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        {}
      ],
      "checklist": {},
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
      "taskIsCurrentlyHalted": true,
      "taskIsCurrentlyHidden": true,
      "taskIsHeading": true,
      "taskKey": "string",
      "taskName": "Ava Chen",
      "taskUrl": "https://example.com",
      "template": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> |  |
| `checklist` | object |  |
| `comments` | array<object> |  |
| `fields` | array<object> |  |
| `tags` | array<object> |  |
| `taskCompletedByEmail` | string |  |
| `taskCompletedByName` | string |  |
| `taskCompletedDateTime` | date |  |
| `taskDueDateTime` | date |  |
| `taskId` | number |  |
| `taskIsCurrentlyHalted` | boolean |  |
| `taskIsCurrentlyHidden` | boolean |  |
| `taskIsHeading` | boolean |  |
| `taskKey` | string |  |
| `taskName` | string |  |
| `taskUrl` | string |  |
| `template` | object |  |

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/checklist/tasks` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks-by-task-key.md) for the provider-specific parameters and requirements.

