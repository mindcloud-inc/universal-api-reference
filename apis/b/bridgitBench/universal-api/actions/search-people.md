# Bridgit Bench: Search People



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-people?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&predicates.state=Active&predicates.relativeDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "predicates.state": "Active",
  "predicates.relativeDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-people?${params}`, {
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
| `accountId` | number | yes | The Account ID |
| `predicates` | object | no |  |
| `predicates.personIds[]` | array<number> | no |  |
| `predicates.state` | list<string> | yes | One of: `Active`, `All`, `Deactivated`. |
| `predicates.email` | string | no |  |
| `predicates.uniqueId` | string | no |  |
| `predicates.relativeDate` | date | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/Persons/_filter` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.

