# Bridgit Bench: List Projects



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-projects?${params}`, {
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
| `name` | string | no | Name filter that affects whether or not to return projects back with/without the name contains partial match (Default: Empty) |
| `issues` | list<number> | no | State filter that affects whether or not to return projects back with/without or any issues (Default: All) One of: `0`, `1`, `2`. Default: `2`. |
| `ids` | number | no | Optional comma delimited list of project IDs to filter the result on Accepts multiple values in one string, delimited by `,`. |
| `projectState` | list<string> | no | Optional comma delimited list for filtering results by project state. One of: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. Accepts multiple values in one string, delimited by `,`. Default: `All`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeProjectNumber` | boolean | no | Whether to include the Project Number field in the response (Default: false) Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/Projects` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

