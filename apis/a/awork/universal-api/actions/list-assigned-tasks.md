# Awork: List Assigned Tasks

Retrieves assigned tasks from Awork.

```
GET https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-assigned-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-assigned-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-assigned-tasks?${params}`, {
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
| `inProgress` | boolean | no | Whether to return only tasks currently in progress. |
| `assignedOnFrom` | string | no | The start date and time for filtering by assignment date. If set, tasks are returned only when the assignment date is greater or equal than this value. Example: `2026-03-20T00:00:00Z`. |
| `assignedOnTo` | string | no | The end date and time for filtering by assignment date. If set, tasks are returned only when the assignment date is less or equal than this value. Example: `2026-03-27T00:00:00Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Awork API returns.

## Native endpoint

Through the native Awork API, this operation is `GET /me/assignedtasks` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assigned-tasks.md) for the provider-specific parameters and requirements.

