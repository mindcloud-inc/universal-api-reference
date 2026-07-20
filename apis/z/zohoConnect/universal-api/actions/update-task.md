# Zoho Connect: Update Task

Updates an existing task in Zoho Connect.

```
PUT https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "priority": "string",
  "scopeID": "string",
  "taskId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "priority": "string",
    "scopeID": "string",
    "taskId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeId` | string | no | Comma-separated user IDs to assign to the task. Accepts multiple values in one string, delimited by `,`. |
| `desc` | string | no | Updated task description. |
| `edate` | number | no | Due date day. |
| `emonth` | number | no | Due date month. |
| `eyear` | number | no | Due date year. |
| `isClearDueDate` | boolean | no | Clear the task due date. |
| `priority` | string | yes | Priority level: None, Low, Medium, or High. |
| `removeAssigneeId` | string | no | Comma-separated user IDs to remove from the task. Accepts multiple values in one string, delimited by `,`. |
| `scopeID` | string | yes | ID of the network where the task exists. |
| `status` | number | no | Task status code: 0, 1, 2, 3, or 4. |
| `taskId` | string | yes | ID of the task to update. |
| `title` | string | yes | Updated task title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updateTask": {
        "reason": "string",
        "result": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updateTask.reason` | string |  |
| `updateTask.result` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/updateTask` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

