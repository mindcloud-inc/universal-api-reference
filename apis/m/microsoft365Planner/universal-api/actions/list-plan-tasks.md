# Microsoft 365 Planner: List Plan Tasks



```
GET https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-plan-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-plan-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&planId=xqQg5FS2LkCp935s-FIFm2QAFkHM" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-plan-tasks?${params}`, {
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
| `planId` | string | yes | Planner plan ID whose tasks should be listed. Example: `xqQg5FS2LkCp935s-FIFm2QAFkHM`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucketId": "string",
      "dueDateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "percentComplete": 1,
      "planId": "string",
      "priority": 1,
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketId` | string |  |
| `dueDateTime` | date |  |
| `id` | string |  |
| `percentComplete` | number |  |
| `planId` | string |  |
| `priority` | number |  |
| `startDateTime` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `GET /v1.0/planner/plans/{{planId}}/tasks` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-plan-tasks.md) for the provider-specific parameters and requirements.

