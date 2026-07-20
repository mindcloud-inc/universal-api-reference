# actiTIME: Get Task

Retrieves a specific task from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-task?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-task?${params}`, {
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
| `id` | number | yes | Task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedActions": {
        "canDelete": true,
        "canModify": true
      },
      "created": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "customerName": "Ava Chen",
      "deadline": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "estimatedTime": 1,
      "id": 1,
      "name": "Ava Chen",
      "projectId": 1,
      "projectName": "Ava Chen",
      "status": "string",
      "typeOfWorkId": 1,
      "typeOfWorkName": "Ava Chen",
      "url": "https://example.com",
      "workflowStatusId": 1,
      "workflowStatusName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedActions.canDelete` | boolean | Whether the task can be deleted. |
| `allowedActions.canModify` | boolean | Whether the task can be modified. |
| `created` | date | Creation date and time. |
| `customerId` | number | Customer identifier. |
| `customerName` | string | Customer name. |
| `deadline` | date | Task deadline. |
| `description` | string | Task description. |
| `estimatedTime` | number | Estimated time in minutes. |
| `id` | number | Unique task identifier. |
| `name` | string | Task name. |
| `projectId` | number | Project identifier. |
| `projectName` | string | Project name. |
| `status` | string | Task status. |
| `typeOfWorkId` | number | Type of work identifier. |
| `typeOfWorkName` | string | Type of work name. |
| `url` | string | Task URL. |
| `workflowStatusId` | number | Workflow status identifier. |
| `workflowStatusName` | string | Workflow status name. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /tasks/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

