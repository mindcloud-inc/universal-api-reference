# Create Project Role with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/roles`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Role](https://developers.gobridgit.com/reference/projectroles_add)

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
| `name` | body | `string` | yes | — |
| `taskId` | body | `string` | no | — |
| `startDate` | body | `date` | yes | — |
| `endDate` | body | `date` | yes | — |
| `skillSet[]` | body | `array<number>` | yes | — |
| `note` | body | `string` | no | Maximum length: 250. |
| `categoryId` | body | `number` | no | — |
| `billable` | body | `boolean` | yes | — |
| `allocations[]` | body | `array<object>` | no | — |
| `allocations[].startDate` | body | `date` | yes | — |
| `allocations[].endDate` | body | `date` | yes | — |
| `allocations[].allocatedPercent` | body | `number` | yes | — |
| `roleTagIds[]` | body | `array<number>` | no | — |
| `assignmentBreakdownBy` | body | `list<string>` | no | Accepted values: `Custom`, `Monthly`, `Phases`, `Weekly`. |
