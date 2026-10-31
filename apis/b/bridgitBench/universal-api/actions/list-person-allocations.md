# Bridgit Bench: List Person Allocations



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-allocations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-allocations?connectionId=$CONNECTION_ID&accountId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-person-allocations?${params}`, {
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
| `id` | number | yes | The Person's ID |
| `relativeDate` | date | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `start` | date | no | Start date to filter allocations from |
| `end` | date | no | End date to filter allocations to |
| `roleId` | number | no | Optional parameter to get allocations for a specific role |
| `projectState` | list<string> | no | Optional parameter for filtering results by project state. One of: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. Default: `All`. |
| `type` | list<string> | no | Optional parameter Salaried role type to filter results by (Default to Operations) One of: `All`, `Operations`, `Preconstruction`. Default: `Operations`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/Persons/:id/allocations` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-person-allocations.md) for the provider-specific parameters and requirements.

