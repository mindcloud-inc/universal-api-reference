# Clockify: List Project Tasks

Lists all project tasks in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-project-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-project-tasks?${params}`, {
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
| `projectId` | string | yes |  |
| `name` | string | no |  |
| `strictNameSearch` | boolean | no |  |
| `isActive` | boolean | no |  |

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

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/projects/:projectId/tasks` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-tasks.md) for the provider-specific parameters and requirements.

