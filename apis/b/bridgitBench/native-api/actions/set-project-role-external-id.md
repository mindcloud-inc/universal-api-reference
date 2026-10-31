# Set Project Role External ID with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/roles/:id/externalId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Set Project Role External ID](https://developers.gobridgit.com/reference/projectroles_setexternalid)

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
| `id` | path | `number` | yes | The Role ID |
| `externalId` | body | `string` | no | — |
