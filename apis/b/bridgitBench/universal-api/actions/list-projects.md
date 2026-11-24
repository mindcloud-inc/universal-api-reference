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

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "colour": "string",
      "startDate": "string",
      "endDate": "string",
      "startTime": "string",
      "endTime": "string",
      "workDays": [
        1
      ],
      "hoursPerWeek": 1,
      "state": "string",
      "winPercent": 1,
      "unfilledRoles": 1,
      "totalRoles": 1,
      "unfilledHourlyRoles": 1,
      "totalHourlyRoles": 1,
      "totalTasks": 1,
      "unfilledTaskRoles": 1,
      "totalTaskRoles": 1,
      "issuesCount": 1,
      "lastModifiedOn": "string",
      "type": "string",
      "currentPhases": [
        {}
      ],
      "phases": [
        {}
      ],
      "groupings": [
        1
      ],
      "description": "string",
      "truncatedDescription": "string",
      "externalId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `colour` | string |  |
| `startDate` | string |  |
| `endDate` | string |  |
| `startTime` | string |  |
| `endTime` | string |  |
| `workDays` | array<number> |  |
| `hoursPerWeek` | number |  |
| `state` | string |  |
| `winPercent` | number |  |
| `unfilledRoles` | number |  |
| `totalRoles` | number |  |
| `unfilledHourlyRoles` | number |  |
| `totalHourlyRoles` | number |  |
| `totalTasks` | number |  |
| `unfilledTaskRoles` | number |  |
| `totalTaskRoles` | number |  |
| `issuesCount` | number |  |
| `lastModifiedOn` | string |  |
| `type` | string |  |
| `currentPhases` | array<object> |  |
| `phases` | array<object> |  |
| `groupings` | array<number> |  |
| `description` | string |  |
| `truncatedDescription` | string |  |
| `externalId` | string |  |

## Native endpoint

Through the native Bridgit Bench API, this operation is `GET /rp/api/v1/accounts/:accountId/Projects` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

