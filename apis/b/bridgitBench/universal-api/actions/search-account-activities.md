# Bridgit Bench: Search Account Activities



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-account-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-account-activities?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&predicates.personIds%5B%5D=1&predicates.projectIds%5B%5D=1&predicates.triggeredByUserIds%5B%5D=1&predicates.activityTypes%5B%5D=string&predicates.triggeredByIntegrations=true&predicates.triggeredByUsers=true&predicates.groupingIds%5B%5D=1&predicates.includeBlankGroupIds=true&predicates.activityTypeSearch=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "predicates.personIds[]": "1",
  "predicates.projectIds[]": "1",
  "predicates.triggeredByUserIds[]": "1",
  "predicates.activityTypes[]": "string",
  "predicates.triggeredByIntegrations": "true",
  "predicates.triggeredByUsers": "true",
  "predicates.groupingIds[]": "1",
  "predicates.includeBlankGroupIds": "true",
  "predicates.activityTypeSearch": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-account-activities?${params}`, {
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
| `accountId` | number | yes | The account ID (must be greater than zero) |
| `predicates` | object | no |  |
| `predicates.personIds[]` | array<number> | yes |  |
| `predicates.projectIds[]` | array<number> | yes |  |
| `predicates.happenedFrom` | date | no |  |
| `predicates.happenedTo` | date | no |  |
| `predicates.triggeredByUserIds[]` | array<number> | yes |  |
| `predicates.activityTypes[]` | array<string> | yes |  |
| `predicates.triggeredByIntegrations` | boolean | yes |  |
| `predicates.triggeredByUsers` | boolean | yes |  |
| `predicates.groupingIds[]` | array<number> | yes |  |
| `predicates.includeBlankGroupIds` | boolean | yes |  |
| `predicates.activityTypeSearch` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/activities/_filter` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-account-activities.md) for the provider-specific parameters and requirements.

