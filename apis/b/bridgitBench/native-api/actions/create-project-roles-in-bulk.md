# Create Project Roles in Bulk with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/roles/bulk`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Roles in Bulk](https://developers.gobridgit.com/reference/projectroles_bulkadd)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the role belongs to |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].name` | body | `string` | yes | — |
| `payload[].taskId` | body | `string` | no | — |
| `payload[].startDate` | body | `date` | yes | — |
| `payload[].endDate` | body | `date` | yes | — |
| `payload[].skillSet[]` | body | `array<number>` | yes | — |
| `payload[].note` | body | `string` | no | Maximum length: 250. |
| `payload[].categoryId` | body | `number` | no | — |
| `payload[].billable` | body | `boolean` | yes | — |
| `payload[].allocations[]` | body | `array<object>` | no | — |
| `payload[].allocations[].startDate` | body | `date` | yes | — |
| `payload[].allocations[].endDate` | body | `date` | yes | — |
| `payload[].allocations[].allocatedPercent` | body | `number` | yes | — |
| `payload[].roleTagIds[]` | body | `array<number>` | no | — |
| `payload[].assignmentBreakdownBy` | body | `list<string>` | no | Accepted values: `Custom`, `Monthly`, `Phases`, `Weekly`. |
