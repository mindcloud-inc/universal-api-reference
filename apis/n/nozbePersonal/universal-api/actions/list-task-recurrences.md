# Nozbe Personal: List Task Recurrences

Retrieves accessible task recurrences from Nozbe Personal.

```
GET https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-task-recurrences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-task-recurrences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-task-recurrences?${params}`, {
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
| `projectId` | string | no |  |
| `currentTaskId` | string | no |  |
| `fields` | string | no |  |
| `sortBy` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nozbe Personal API returns.

## Native endpoint

Through the native Nozbe Personal API, this operation is `GET /task_recurrences` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-task-recurrences.md) for the provider-specific parameters and requirements.

