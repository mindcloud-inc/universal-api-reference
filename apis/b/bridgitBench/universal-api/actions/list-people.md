# Bridgit Bench: List People



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-people?${params}`, {
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
| `relativeDate` | date | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `email` | string | no | Filter user with email |
| `state` | list<string> | no | If specified and not 'Unknown', only include people matching the given state. The available values are defined as follows: - Unknown: By default, includes only Active people. - Active: include only Active people - Deactivated: include only Deactivated people - All: include all people, regardless of state One of: `Active`, `All`, `Deactivated`. Default: `Active`. |
| `ids` | number | no | Optional paramater of comma delimited ids for filtering results based on the person IDs provided Accepts multiple values in one string, delimited by `,`. |
| `uniqueId` | string | no | Optional paramater of unique identifier for filtering results based on the person unique identifier provided |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/Persons` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

