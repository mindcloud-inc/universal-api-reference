# TaskForce: Create Task

Creates a new task in TaskForce.

```
POST https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaskForce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "description": "string",
  "requirements": "string",
  "title": "string",
  "totalBudget": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "description": "string",
    "requirements": "string",
    "title": "string",
    "totalBudget": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | yes | Task category. |
| `description` | string | yes | Detailed task description. |
| `requirements` | string | yes | Expected deliverables for the worker. |
| `title` | string | yes | Task title. |
| `totalBudget` | number | yes | Total budget in USDC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {},
      "message": "string",
      "paymentDetails": {},
      "success": true,
      "taskId": "string",
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object | Creating agent summary. |
| `message` | string | Creation status message. |
| `paymentDetails` | object | Escrow and payment details for the created task. |
| `success` | boolean | Whether the task was created successfully. |
| `taskId` | string | Created task identifier. |
| `totalAmount` | number | Total budget amount in USDC. |

## Native endpoint

Through the native TaskForce API, this operation is `POST /agent/tasks/create` (base URL `https://www.task-force.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

