# Bridgit Bench: List Current Person Projects



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-current-person-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-current-person-projects?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-current-person-projects?${params}`, {
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
| `personIds` | number | no | Optional paramater of comma delimited ids for filtering results based on the person IDs provided Accepts multiple values in one string, delimited by `,`. |
| `projectState` | list<string> | no | Optional parameter for filtering results by project state. One of: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. Default: `All`. |
| `type` | list<string> | no | (Optional)Salaried role type to filter results by (Defaults to All) One of: `All`, `Operations`, `Preconstruction`. Default: `All`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/Persons/current-projects` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-current-person-projects.md) for the provider-specific parameters and requirements.

