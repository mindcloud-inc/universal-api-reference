# ServiceM8: Create Task



```
POST https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "relatedObject": "string",
  "relatedObjectUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "relatedObject": "string",
    "relatedObjectUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name or title of the task. |
| `taskDetails` | string | no | Detailed description of the task. |
| `dueDate` | date | no | The date by which the task should be completed. |
| `relatedObject` | string | yes | The object class this task is related to. |
| `relatedObjectUuid` | string | yes | UUID of the specific object instance this task is related to. |
| `assignedToStaffUuid` | string | no | UUID of the staff member assigned to complete this task. |
| `taskComplete` | string | no | Whether the task has been completed. |
| `completedTimestamp` | date | no | The date and time when the task was marked as complete. |
| `completedByStaffUuid` | string | no | UUID of the staff member who marked the task as complete. |
| `createdByStaffUuid` | string | no | UUID of the staff member who created the task. |
| `uuid` | string | no | Optional UUID for record creation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recordUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recordUuid` | string | UUID of the created task. |

## Native endpoint

Through the native ServiceM8 API, this operation is `POST /api_1.0/task.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

