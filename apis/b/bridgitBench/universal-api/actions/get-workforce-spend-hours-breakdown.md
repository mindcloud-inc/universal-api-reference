# Bridgit Bench: Get Workforce Spend Hours Breakdown



```
GET https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-workforce-spend-hours-breakdown
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-workforce-spend-hours-breakdown?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=1&projectId=1&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z&period=Annual&bounded=true&roleNameIds%5B%5D=1&roleType=All&salariedRoleType=All&opsPreconFilter=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "1",
  "projectId": "1",
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "period": "Annual",
  "bounded": "true",
  "roleNameIds[]": "1",
  "roleType": "All",
  "salariedRoleType": "All",
  "opsPreconFilter": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/get-workforce-spend-hours-breakdown?${params}`, {
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
| `projectId` | number | yes | The project ID the workforce belongs to |
| `startDate` | date | yes |  |
| `endDate` | date | yes |  |
| `period` | list<string> | yes | One of: `Annual`, `Month`, `Quarter`, `Week`. |
| `bounded` | boolean | yes |  |
| `roleNameIds[]` | array<number> | yes | RoleNameIds to filter by. [] for all. [1, 2, 3] |
| `roleType` | list<string> | yes | RoleType to filter by. Salaried by default. Hourly is not supported. One of: `All`, `Hourly`, `Salaried`. |
| `salariedRoleType` | list<string> | yes | SalariedRoleType to filter by. All by default. One of: `All`, `Operations`, `Preconstruction`. |
| `opsPreconFilter` | list<number> | yes | ResourcePlanning.Contracts.BreakdownRequest.OpsPreconFilter to filter by. ResourcePlanning.Contracts.OpsPreconFilter.OperationsPrecon by default. One of: `0`, `1`, `2`, `3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/projects/:projectId/workforce-spend-reports/hours-breakdown` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-workforce-spend-hours-breakdown.md) for the provider-specific parameters and requirements.

