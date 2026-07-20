# Clockify: Update Project Task

Updates an existing project task in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-project-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-project-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "projectId": "string",
  "taskId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-project-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "projectId": "string",
    "taskId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `projectId` | string | yes |  |
| `taskId` | string | yes |  |
| `containsAssignee` | boolean | no |  |
| `membershipStatus` | string | no |  |
| `name` | string | yes |  |
| `assigneeId` | string | no |  |
| `assigneeIds[]` | array<string> | no |  |
| `billable` | boolean | no |  |
| `budgetEstimate` | number | no |  |
| `estimate` | string | no |  |
| `status` | string | no |  |
| `userGroupIds[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": "string",
      "assigneeIds": [
        "string"
      ],
      "billable": true,
      "budgetEstimate": 1,
      "costRate": {},
      "duration": "string",
      "estimate": "string",
      "hourlyRate": {},
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "status": "string",
      "userGroupIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | string |  |
| `assigneeIds` | array<string> |  |
| `billable` | boolean |  |
| `budgetEstimate` | number |  |
| `costRate` | object |  |
| `duration` | string |  |
| `estimate` | string |  |
| `hourlyRate` | object |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `userGroupIds` | array<string> |  |

## Native endpoint

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/projects/:projectId/tasks/:taskId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-task.md) for the provider-specific parameters and requirements.

