# Bridgit Bench: List Account Hourly Roles



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-hourly-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-hourly-roles?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-account-hourly-roles?${params}`, {
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
| `id` | number | yes | The Account ID |
| `relativeDate` | date | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `projectId` | number | no | (Optional) Filter role(s) for specified project ID |
| `filledState` | list<number> | no | (Optional) Filters the result by the filled state of the roles One of: `0`, `1`, `2`. Default: `2`. |
| `roleIds` | number | no | (Optional) Filters the result to contain roles that match the ids passed in. Works as an AND with filledState and roleNameIds Accepts multiple values as an array. |
| `roleNameIds` | number | no | (Optional) Filters the result to contain roles that match the ids passed in. Works as an AND with filledState and roleIds Accepts multiple values as an array. |
| `projectState` | list<string> | no | (Optional) Filters the result by the state of the project the role is on One of: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. Default: `All`. |
| `roleState` | list<string> | no | (Optional) Filters the result by the state of the role dates: Current, Upcoming, Past, or All One of: `All`, `Current`, `Past`, `Upcoming`. Default: `All`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/Accounts/:id/hourly-roles` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-hourly-roles.md) for the provider-specific parameters and requirements.

