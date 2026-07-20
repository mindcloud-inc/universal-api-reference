# TMetric: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-tasks?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/list-tasks?${params}`, {
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
| `accountId` | number | yes | Workspace identifier. |
| `afterDate` | date | no | Return tasks due on or after this date. |
| `assignee` | number | no | User identifier where 0 is unassigned. |
| `assigneeGroup` | number | no | Team identifier. |
| `beforeDate` | date | no | Return tasks due on or before this date. |
| `clientList` | number<number> | no | List of client identifiers. Accepts multiple values in one string, delimited by `,`. |
| `completed` | boolean | no | Filter by completion status. |
| `creator` | number | no | User identifier who created the task. |
| `projectList` | number<number> | no | List of project identifiers. Accepts multiple values in one string, delimited by `,`. |
| `source` | string | no | Task source filter. |
| `tagList` | number<number> | no | List of tag identifiers. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "creator": {
        "iconUrl": "https://example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "dueDate": "string",
      "estimatedMinutes": "string",
      "id": 1,
      "isCompleted": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "project": {
        "iconUrl": "https://example.com",
        "id": 1,
        "invoiceMethod": "string",
        "isBillable": true,
        "name": "Ava Chen",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `creator.iconUrl` | string |  |
| `creator.id` | number |  |
| `creator.name` | string |  |
| `dueDate` | string |  |
| `estimatedMinutes` | string |  |
| `id` | number |  |
| `isCompleted` | boolean |  |
| `modified` | date |  |
| `name` | string |  |
| `project.iconUrl` | string |  |
| `project.id` | number |  |
| `project.invoiceMethod` | string |  |
| `project.isBillable` | boolean |  |
| `project.name` | string |  |
| `project.status` | string |  |

## Native endpoint

Through the native TMetric API, this operation is `GET /accounts/:accountId/tasks` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

