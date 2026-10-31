# Bridgit Bench: Search Accounts



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0&predicates.accountIds%5B%5D=1&predicates.state=Active&sort.sortBy=0&sort.direction=Asc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "predicates.accountIds[]": "1",
  "predicates.state": "Active",
  "sort.sortBy": "0",
  "sort.direction": "Asc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-accounts?${params}`, {
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
| `predicates` | object | no |  |
| `predicates.accountIds[]` | array<number> | yes |  |
| `predicates.state` | list<string> | yes | One of: `Active`, `All`, `Deactivated`. |
| `predicates.name` | string | no |  |
| `predicates.organizationId` | string | no |  |
| `predicates.isDemo` | boolean | no |  |
| `sort` | object | no |  |
| `sort.sortBy` | list<number> | yes | One of: `0`, `1`, `2`, `3`, `4`, `5`. |
| `sort.direction` | list<string> | yes | One of: `Asc`, `Desc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/Accounts/_filter` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-accounts.md) for the provider-specific parameters and requirements.

