# actiTIME: List Tasks

Retrieves a list of tasks from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-tasks?${params}`, {
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
| `customerIds` | string | no | Comma-separated customer ids to retrieve tasks from. |
| `ids` | string | no | Comma-separated ids of tasks to be returned. |
| `includeReferenced` | string | no | Comma-separated referenced objects to include. |
| `name` | string | no | Exact task name match, case-insensitive. |
| `projectIds` | string | no | Comma-separated project ids to retrieve tasks from. |
| `sort` | string | no | Sorting tokens like +name or -status. |
| `status` | string | no | Task status filter such as open or completed. |
| `typeOfWorkIds` | string | no | Comma-separated type of work ids associated with tasks to be returned. |
| `words` | string | no | Return tasks containing all given words in the name. |
| `workflowStatusIds` | string | no | Comma-separated workflow status ids associated with tasks to be returned. |

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

Through the native actiTIME API, this operation is `GET /tasks` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

