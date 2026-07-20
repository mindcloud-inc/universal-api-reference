# Grand Avenue Software: List Deviation Requests

Retrieves deviation requests from Grand Avenue Software.

```
GET https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/list-deviation-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grand Avenue Software `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/list-deviation-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/list-deviation-requests?${params}`, {
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
| `filter` | string | no | e.g. `UpdatedTimestamp > 2025-12-18T00:00:00.000Z` |
| `select` | list<string> | no | Accepts multiple values in one string. |
| `expand` | list<string> | no | Accepts multiple values in one string. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Grand Avenue Software API returns.

## Native endpoint

Through the native Grand Avenue Software API, this operation is `GET /DeviationRequests` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deviation-requests.md) for the provider-specific parameters and requirements.

