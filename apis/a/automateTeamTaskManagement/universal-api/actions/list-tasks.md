# Automate Team - Task Management: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Automate Team - Task Management `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceFilter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceFilter": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/automateTeamTaskManagement/latest/actions/list-tasks?${params}`, {
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
| `workspaceFilter` | string | yes | PostgREST filter for the workspace id, for example eq.33371. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskIdFilter` | string | no | Optional PostgREST filter for a task id, for example eq.12345. |
| `titleFilter` | string | no | Optional PostgREST filter for task titles, for example ilike.*follow-up*. |
| `statusFilter` | string | no | Optional PostgREST filter for status, for example eq.Pending. |
| `priorityFilter` | string | no | Optional PostgREST filter for priority, for example eq.High. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "frequency": "string",
      "id": "string",
      "priority": "string",
      "status": "string",
      "target_date": "2026-05-07T12:00:00.000Z",
      "task_id": "string",
      "title": "string",
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `frequency` | string |  |
| `id` | string |  |
| `priority` | string |  |
| `status` | string |  |
| `target_date` | date |  |
| `task_id` | string |  |
| `title` | string |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Automate Team - Task Management API, this operation is `GET /rest/v1/t_all_tasks` (base URL `https://api.automatebusiness.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

