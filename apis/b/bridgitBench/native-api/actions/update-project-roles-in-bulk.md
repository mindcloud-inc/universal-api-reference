# Update Project Roles in Bulk with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/roles/bulk`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Project Roles in Bulk](https://developers.gobridgit.com/reference/projectroles_bulkpatchupdate)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | — |
| `projectId` | path | `number` | yes | — |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].id` | body | `number` | yes | — |
| `payload[].taskId` | body | `string` | no | When taskId is included, the role is a task role. The taskId cannot be changed. |
| `payload[].name` | body | `string` | no | — |
| `payload[].startDate` | body | `date` | no | — |
| `payload[].endDate` | body | `date` | no | — |
| `payload[].skillSet[]` | body | `array<number>` | no | — |
| `payload[].note` | body | `string` | no | Maximum length: 250. |
| `payload[].categoryId` | body | `number` | no | — |
| `payload[].billable` | body | `boolean` | no | — |
| `payload[].allocations[]` | body | `array<object>` | no | — |
| `payload[].allocations[].startDate` | body | `date` | yes | — |
| `payload[].allocations[].endDate` | body | `date` | yes | — |
| `payload[].allocations[].allocatedPercent` | body | `number` | yes | — |
| `payload[].removeSetup` | body | `boolean` | yes | — |
| `payload[].expandAllocations` | body | `boolean` | yes | — |
| `payload[].shiftDates` | body | `boolean` | yes | — |
| `payload[].roleTagIds[]` | body | `array<number>` | no | — |
| `payload[].crewId` | body | `number` | no | — |
