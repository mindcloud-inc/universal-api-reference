# CheckFlow: Get Task Details



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-task-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-task-details?connectionId=$CONNECTION_ID&checklistId=1234&taskKey=07072bc4-f1eb-4536-819a-1ddb7dc109a1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checklistId": "1234",
  "taskKey": "07072bc4-f1eb-4536-819a-1ddb7dc109a1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-task-details?${params}`, {
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
| `checklistId` | number | yes | The ID of the checklist that contains the task. Example: `1234`. |
| `taskKey` | string | yes | The key of the task. Example: `07072bc4-f1eb-4536-819a-1ddb7dc109a1`. |

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

Through the native CheckFlow API, this operation is `GET /api/task/details` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-details.md) for the provider-specific parameters and requirements.

