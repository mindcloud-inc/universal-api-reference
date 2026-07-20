# Nagaris: List Client Groups

Finds client groups in Nagaris by filters.

```
GET https://connect.mindcloud.co/v1/universal/nagaris/latest/actions/list-client-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nagaris `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nagaris/latest/actions/list-client-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nagaris/latest/actions/list-client-groups?${params}`, {
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
| `search` | string | no | Search across client group name and code fields. |
| `name` | string | no | Filter client groups by name contains. |
| `status` | list | no | Filter by client group status. One of: `0`, `1`, `2`, `3`. |
| `isFinalised` | boolean | no | Filter by whether the client group is finalised. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nagaris API returns.

## Native endpoint

Through the native Nagaris API, this operation is `GET /client-groups/` (base URL `https://core.nagaris.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-client-groups.md) for the provider-specific parameters and requirements.

