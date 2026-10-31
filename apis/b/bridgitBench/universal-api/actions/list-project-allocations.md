# Bridgit Bench: List Project Allocations



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-project-allocations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-project-allocations?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-project-allocations?${params}`, {
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
| `projectId` | number | yes | The Project ID |
| `relativeDate` | date | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `personstate` | list<string> | no | State of persons to filter results by (Default Active) One of: `Active`, `All`, `Deactivated`. Default: `Active`. |
| `daysUntilTimeOff` | number | no | Used to calculate the upcoming TimeOff unavailabilities based on the relativeDate Default: `15`. |
| `type` | list<string> | no | Salaried role type to filter results by (Default to Operations) One of: `All`, `Operations`, `Preconstruction`. Default: `Operations`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/projects/:projectId/Allocations` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-allocations.md) for the provider-specific parameters and requirements.

