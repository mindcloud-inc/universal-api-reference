# Avaza: List Tasks

Retrieves tasks from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-tasks?${params}`, {
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
| `updatedafter` | date | no | Optional filter to records updated after a specific date. |
| `iscomplete` | boolean | no | Optional filter to only display tasks linked to a Task Status where isComplete=false, or where isComplete=true |
| `projectid` | number | no | Optional filter to only display tasks belonging to a specific ProjectID |
| `taskstatuscode` | string | no | Optional filter to only display tasks with a specific status |
| `taskprioritycode` | string | no | Optional filter to only display tasks with a specific priority |
| `duedatefrom` | date | no | Optional filter to only display tasks with a Due Date after DueDateFrom |
| `duedateto` | date | no | Optional filter to only display tasks with a Due Date before DueDateTo |
| `assignedtouserids` | list<number> | no | Optional filter to only display tasks with at least one of the provided UserIDs set as the Assigned User. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/Task` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

