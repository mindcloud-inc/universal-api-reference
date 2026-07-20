# CheckFlow: Update Task Status



```
PUT https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/update-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/update-task-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "5678",
  "status": "Complete",
  "modifiedByUserId": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/update-task-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "5678",
    "status": "Complete",
    "modifiedByUserId": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | The ID of the task to update. Example: `5678`. |
| `status` | string | yes | The new status. Values: Complete, Incomplete, NotApplicable. Example: `Complete`. |
| `modifiedByUserId` | number | yes | The ID of the user updating the task status. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        {}
      ],
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
      "taskIsComplete": true,
      "taskIsCurrentlyHalted": true,
      "taskIsCurrentlyHidden": true,
      "taskIsHeading": true,
      "taskIsNotApplicable": true,
      "taskKey": "string",
      "taskName": "Ava Chen",
      "taskNotApplicableByEmail": "ava@example.com",
      "taskNotApplicableByName": "Ava Chen",
      "taskNotApplicableDateTime": "2026-05-07T12:00:00.000Z",
      "taskUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> |  |
| `comments` | array<object> |  |
| `fields` | array<object> |  |
| `tags` | array<object> |  |
| `taskCompletedByEmail` | string |  |
| `taskCompletedByName` | string |  |
| `taskCompletedDateTime` | date |  |
| `taskDueDateTime` | date |  |
| `taskId` | number |  |
| `taskIsComplete` | boolean |  |
| `taskIsCurrentlyHalted` | boolean |  |
| `taskIsCurrentlyHidden` | boolean |  |
| `taskIsHeading` | boolean |  |
| `taskIsNotApplicable` | boolean |  |
| `taskKey` | string |  |
| `taskName` | string |  |
| `taskNotApplicableByEmail` | string |  |
| `taskNotApplicableByName` | string |  |
| `taskNotApplicableDateTime` | date |  |
| `taskUrl` | string |  |

## Native endpoint

Through the native CheckFlow API, this operation is `PUT /api/task/status` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-status.md) for the provider-specific parameters and requirements.

