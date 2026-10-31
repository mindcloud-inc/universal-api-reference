# Update Project Phases in Bulk with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/phases/bulk`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Project Phases in Bulk](https://developers.gobridgit.com/reference/projectsphases_bulkupdate)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The Project ID |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].id` | body | `number` | yes | — |
| `payload[].startDate` | body | `date` | no | — |
| `payload[].endDate` | body | `date` | no | — |
| `payload[].shiftDates` | body | `boolean` | yes | — |
