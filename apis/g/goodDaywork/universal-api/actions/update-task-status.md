# GoodDay.work: Update Task Status

Updates the status of a GoodDay.work task.

```
PUT https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/update-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/update-task-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "userId": "string",
  "statusId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/update-task-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "userId": "string",
    "statusId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | GoodDay task ID. |
| `userId` | string | yes | User on behalf of whom status update is executed. |
| `statusId` | string | yes | New status ID. |
| `message` | string | no | Optional status comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": "string",
      "createdByUserId": "string",
      "id": "string",
      "projectId": "string",
      "taskStatusId": "string",
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
| `id` | string | Task ID. |
| `projectId` | string | Associated project ID. |
| `taskStatusId` | string | Task status ID. |
| `title` | string | Task title. |

## Native endpoint

Through the native GoodDay.work API, this operation is `PUT /task/:taskId/status` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-status.md) for the provider-specific parameters and requirements.

