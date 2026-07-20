# Streak: List Box Tasks

Retrieves tasks for a box in Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-box-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-box-tasks?connectionId=$CONNECTION_ID&boxKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boxKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-box-tasks?${params}`, {
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
| `boxKey` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Tasks attached to the box. |
| `results[].assignedToSharingEntries` | array<object> | Assignees for the task. |
| `results[].boxKey` | string | The box that owns the task. |
| `results[].creationDate` | date | When the task was created. |
| `results[].creatorKey` | string | The user who created the task. |
| `results[].creatorSharingEntry` | object | The sharing entry for the task creator. |
| `results[].isDraft` | boolean | Whether the task is still a draft. |
| `results[].key` | string | The task key. |
| `results[].lastSavedTimestamp` | date | When the task was last saved. |
| `results[].lastStatusChangeDate` | date | When the task status last changed. |
| `results[].pipelineKey` | string | The pipeline that owns the task. |
| `results[].reminderStatus` | string | The reminder status. |
| `results[].sortOrder` | string | The task ordering token. |
| `results[].status` | string | The task status. |
| `results[].text` | string | The task text. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v2/boxes/:boxKey/tasks` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-box-tasks.md) for the provider-specific parameters and requirements.

