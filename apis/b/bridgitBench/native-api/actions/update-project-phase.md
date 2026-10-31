# Update Project Phase with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/phases/:phaseId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Project Phase](https://developers.gobridgit.com/reference/projectsphases_update)

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
| `phaseId` | path | `number` | yes | The Phase ID |
| `startDate` | body | `date` | no | — |
| `endDate` | body | `date` | no | — |
| `shiftDates` | body | `boolean` | yes | — |
