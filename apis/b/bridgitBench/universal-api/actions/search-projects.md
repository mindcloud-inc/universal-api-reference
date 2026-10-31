# Bridgit Bench: Search Projects



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&predicates.projectState=Active&predicates.issues=0&predicates.relativeDate=2026-05-07T12%3A00%3A00.000Z&predicates.includeProjectNumber=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "predicates.projectState": "Active",
  "predicates.issues": "0",
  "predicates.relativeDate": "2026-05-07T12:00:00.000Z",
  "predicates.includeProjectNumber": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-projects?${params}`, {
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
| `predicates.projectIds[]` | array<number> | no |  |
| `predicates.projectState` | list<string> | yes | One of: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. |
| `predicates.name` | string | no |  |
| `predicates.issues` | list<number> | yes | One of: `0`, `1`, `2`. |
| `predicates.relativeDate` | date | yes |  |
| `predicates.includeProjectNumber` | boolean | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/Projects/_filter` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-projects.md) for the provider-specific parameters and requirements.

