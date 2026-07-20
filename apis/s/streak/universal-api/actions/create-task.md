# Streak: Create Task

Creates a new task in Streak.

```
POST https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boxKey": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streak/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boxKey": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boxKey` | string | yes |  |
| `text` | string | yes |  |
| `dueDate` | date | no |  |
| `assignedToSharingEntries[].email` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToSharingEntries": [
        {}
      ],
      "boxKey": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "creatorKey": "string",
      "creatorSharingEntry": {},
      "isDraft": true,
      "key": "string",
      "lastSavedTimestamp": "2026-05-07T12:00:00.000Z",
      "lastStatusChangeDate": "2026-05-07T12:00:00.000Z",
      "pipelineKey": "string",
      "reminderStatus": "string",
      "sortOrder": "string",
      "status": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToSharingEntries` | array<object> | Assignees for the task. |
| `boxKey` | string | The box that owns the task. |
| `creationDate` | date | When the task was created. |
| `creatorKey` | string | The user who created the task. |
| `creatorSharingEntry` | object | The sharing entry for the task creator. |
| `isDraft` | boolean | Whether the task is still a draft. |
| `key` | string | The task key. |
| `lastSavedTimestamp` | date | When the task was last saved. |
| `lastStatusChangeDate` | date | When the task status last changed. |
| `pipelineKey` | string | The pipeline that owns the task. |
| `reminderStatus` | string | The reminder status. |
| `sortOrder` | string | The task ordering token. |
| `status` | string | The task status. |
| `text` | string | The task text. |

## Native endpoint

Through the native Streak API, this operation is `POST /api/v2/boxes/:boxKey/tasks` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

