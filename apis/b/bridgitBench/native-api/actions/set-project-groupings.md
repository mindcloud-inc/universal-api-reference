# Set Project Groupings with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/groupings`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Set Project Groupings](https://developers.gobridgit.com/reference/projectgroupings_set)

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
| `payload[]` | body | `array<number>` | yes | — |
