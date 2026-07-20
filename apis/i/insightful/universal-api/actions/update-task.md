# Insightful: Update Task

Updates an existing task in your Insightful account.

```
PUT https://connect.mindcloud.co/v1/universal/insightful/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightful/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billable` | boolean | no | Whether the task is billable. |
| `deadline` | number | no | Task deadline in milliseconds. |
| `description` | string | no | The updated task description. |
| `employees[]` | array<string> | no | Employee IDs assigned to the task. |
| `id` | string | yes | The task ID to update. |
| `name` | string | no | The updated task name. |
| `status` | string | no | The updated task status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "description": "string",
      "employees": [
        "string"
      ],
      "id": "string",
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "priority": "string",
      "projectId": "string",
      "status": "string",
      "teams": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `description` | string |  |
| `employees[]` | string |  |
| `id` | string |  |
| `modelName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `priority` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `teams[]` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Insightful API, this operation is `PUT /task/:id` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

