# GoodDay.work: Create Task

Creates a new task in GoodDay.work.

```
POST https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "title": "string",
  "fromUserId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "title": "string",
    "fromUserId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Task project ID. |
| `title` | string | yes | Task title. |
| `fromUserId` | string | yes | User ID creating the task. |
| `toUserId` | string | no | Assigned or action-required user ID. |
| `estimate` | number | no | Task estimate in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": "string",
      "createdByUserId": "string",
      "dateCreated": "string",
      "estimate": 1,
      "id": "string",
      "projectId": "string",
      "taskStatusId": "string",
      "taskTypeId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUserId` | string | Assigned user ID. |
| `createdByUserId` | string | User who created the task. |
| `dateCreated` | string | Creation timestamp. |
| `estimate` | number | Task estimate in minutes. |
| `id` | string | Created task ID. |
| `projectId` | string | Associated project ID. |
| `taskStatusId` | string | Task status ID. |
| `taskTypeId` | string | Task type ID. |
| `title` | string | Task title. |

## Native endpoint

Through the native GoodDay.work API, this operation is `POST /tasks` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

