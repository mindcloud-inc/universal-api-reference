# Clockify: Delete Project Task

Deletes an existing project task from Clockify.

```
DELETE https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-project-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-project-task?connectionId=$CONNECTION_ID&workspaceId=string&projectId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "projectId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-project-task?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `projectId` | string<string> | yes |  |
| `taskId` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": "string",
      "assigneeIds": [
        [
          "string"
        ]
      ],
      "billable": true,
      "budgetEstimate": 1,
      "costRate": {
        "amount": 1,
        "currency": "string"
      },
      "duration": "string",
      "estimate": "string",
      "hourlyRate": {
        "amount": 1,
        "currency": "https://example.com"
      },
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "status": "string",
      "userGroupIds": [
        [
          "string"
        ]
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
| `assigneeIds[]` | array<string> |  |
| `billable` | boolean |  |
| `budgetEstimate` | number |  |
| `costRate` | object |  |
| `costRate.amount` | number |  |
| `costRate.currency` | string |  |
| `duration` | string |  |
| `estimate` | string |  |
| `hourlyRate` | object |  |
| `hourlyRate.amount` | number |  |
| `hourlyRate.currency` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `userGroupIds[]` | array<string> |  |

## Native endpoint

Through the native Clockify API, this operation is `DELETE workspaces/:workspaceId/projects/:projectId/tasks/:taskId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-task.md) for the provider-specific parameters and requirements.

