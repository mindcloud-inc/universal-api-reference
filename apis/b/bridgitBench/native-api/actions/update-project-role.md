# Update Project Role with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/roles/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Project Role](https://developers.gobridgit.com/reference/projectroles_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID that the role belongs to |
| `id` | path | `number` | yes | The role ID |
| `payload` | body | `object` | yes | — |
| `payload.id` | body | `number` | yes | — |
| `payload.removeSetup` | body | `boolean` | yes | — |
| `payload.expandAllocations` | body | `boolean` | yes | — |
| `payload.shiftDates` | body | `boolean` | yes | — |
| `payload.crewId` | body | `number` | no | — |
| `payload.startTime` | body | `string` | no | — |
| `payload.endTime` | body | `string` | no | — |
| `payload.workDays` | body | `list<number>` | no | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Send multiple values as a array. |
| `payload.name` | body | `string` | yes | — |
| `payload.taskId` | body | `string` | no | — |
| `payload.startDate` | body | `date` | yes | — |
| `payload.endDate` | body | `date` | yes | — |
| `payload.skillSet[]` | body | `array<number>` | yes | — |
| `payload.note` | body | `string` | no | Maximum length: 250. |
| `payload.categoryId` | body | `number` | no | — |
| `payload.billable` | body | `boolean` | yes | — |
| `payload.allocations[]` | body | `array<object>` | no | — |
| `payload.allocations[].startDate` | body | `date` | yes | — |
| `payload.allocations[].endDate` | body | `date` | yes | — |
| `payload.allocations[].allocatedPercent` | body | `number` | yes | — |
| `payload.roleTagIds[]` | body | `array<number>` | no | — |
| `payload.assignmentBreakdownBy` | body | `list<string>` | no | Accepted values: `Custom`, `Monthly`, `Phases`, `Weekly`. |
