# Bridgit Bench: Search Person Collaborations



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-person-collaborations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-person-collaborations?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1&predicates.roleType=All&predicates.salariedRoleType=All" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1",
  "predicates.roleType": "All",
  "predicates.salariedRoleType": "All"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/search-person-collaborations?${params}`, {
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
| `id` | number | yes | The account ID |
| `predicates` | object | no |  |
| `predicates.personIds[]` | array<number> | no |  |
| `predicates.projectId` | number | no |  |
| `predicates.roleType` | list<string> | yes | One of: `All`, `Hourly`, `Salaried`. |
| `predicates.salariedRoleType` | list<string> | yes | One of: `All`, `Operations`, `Preconstruction`. |
| `predicates.roleNameIds[]` | array<number> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/Accounts/:id/collaboration-matrix/_filter` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-person-collaborations.md) for the provider-specific parameters and requirements.

