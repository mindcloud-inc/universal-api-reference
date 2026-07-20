# Ninety.io: Query Rocks

Retrieves rocks from Ninety.io with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/query-rocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/query-rocks?connectionId=$CONNECTION_ID&sortField=string&sortDirection=string&pageSize=1&pageIndex=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sortField": "string",
  "sortDirection": "string",
  "pageSize": "1",
  "pageIndex": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/query-rocks?${params}`, {
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
| `sortField` | string | yes |  |
| `sortDirection` | string | yes |  |
| `pageSize` | number | yes |  |
| `pageIndex` | number | yes |  |
| `teamId` | string | no | Filter Rocks by team Id |
| `userId` | string | no | Filter Rocks by owner user Id |
| `statusCode` | string | no | Filter Rocks by status |
| `levelCode` | string | no | Filter Rocks by level |
| `futureScope` | string | no | Filter by future scope |
| `archived` | boolean | no | True for archived Rocks only, false for active Rocks only |
| `searchText` | string | no | Filter Rocks by title or description text |
| `includeRockGoals` | boolean | no | When true, linked goals are included in the response |
| `userIds` | string | no | Comma-separated list of user Ids to filter Rocks by |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninety.io API returns.

## Native endpoint

Through the native Ninety.io API, this operation is `POST /v1/rocks/query` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-rocks.md) for the provider-specific parameters and requirements.

