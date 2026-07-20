# Clockify: Get Project Task

Retrieves a specific project task from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-project-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-project-task?connectionId=$CONNECTION_ID&workspaceId=string&projectId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "projectId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-project-task?${params}`, {
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
      "assigneeIds": [
        [
          "string"
        ]
      ],
      "billable": true,
      "budgetEstimate": 1,
      "duration": "string",
      "estimate": "string",
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
| `assigneeIds[]` | array |  |
| `billable` | boolean |  |
| `budgetEstimate` | number |  |
| `duration` | string |  |
| `estimate` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `userGroupIds[]` | array |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/projects/:projectId/tasks/:taskId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-task.md) for the provider-specific parameters and requirements.

