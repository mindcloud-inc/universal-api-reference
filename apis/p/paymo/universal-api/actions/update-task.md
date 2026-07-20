# Paymo: Update Task

Updates an existing task in Paymo.

```
PUT https://connect.mindcloud.co/v1/universal/paymo/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paymo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paymo/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | The Paymo task id. |
| `name` | string | no | Updated task name. |
| `description` | string | no | Updated task description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "billingType": "string",
      "code": "string",
      "complete": true,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "flatBilling": true,
      "id": 1,
      "name": "Ava Chen",
      "priority": 1,
      "projectId": 1,
      "statusId": 1,
      "tasklistId": 1,
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "users": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `billingType` | string |  |
| `code` | string |  |
| `complete` | boolean |  |
| `createdOn` | date |  |
| `description` | string |  |
| `flatBilling` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `priority` | number |  |
| `projectId` | number |  |
| `statusId` | number |  |
| `tasklistId` | number |  |
| `updatedOn` | date |  |
| `userId` | number |  |
| `users` | array<number> |  |

## Native endpoint

Through the native Paymo API, this operation is `PUT tasks/:taskId` (base URL `https://app.paymoapp.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

