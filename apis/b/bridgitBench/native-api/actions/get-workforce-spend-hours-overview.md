# Get Workforce Spend Hours Overview with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/workforce-spend-reports/hours-overview`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Get Workforce Spend Hours Overview](https://developers.gobridgit.com/reference/projectworkforcespendreports_getworkforcespendreportsoverviewhours)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the workforce belongs to |
| `startDate` | body | `date` | yes | — |
| `endDate` | body | `date` | yes | — |
| `relativeDate` | body | `date` | yes | — |
| `roleNameIds[]` | body | `array<number>` | yes | RoleNameIds to filter by. [] for all.  [1, 2, 3] |
| `roleType` | body | `list<string>` | yes | RoleType to filter by. Salaried by default. Hourly is not supported. Accepted values: `All`, `Hourly`, `Salaried`. |
| `salariedRoleType` | body | `list<string>` | yes | SalariedRoleType to filter by. All by default. Accepted values: `All`, `Operations`, `Preconstruction`. |
| `opsPreconFilter` | body | `list<number>` | yes | ResourcePlanning.Contracts.OverviewRequest.OpsPreconFilter to filter by. ResourcePlanning.Contracts.OpsPreconFilter.OperationsPrecon by default. Accepted values: `0`, `1`, `2`, `3`. |
