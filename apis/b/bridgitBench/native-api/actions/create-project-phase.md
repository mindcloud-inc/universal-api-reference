# Create Project Phase with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/phases`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Phase](https://developers.gobridgit.com/reference/projectsphases_add)

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
| `id` | body | `number` | yes | — |
| `startDate` | body | `date` | yes | — |
| `endDate` | body | `date` | yes | — |
