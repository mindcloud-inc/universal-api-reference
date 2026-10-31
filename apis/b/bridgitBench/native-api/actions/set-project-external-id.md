# Set Project External ID with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/Projects/:id/externalId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Set Project External ID](https://developers.gobridgit.com/reference/projects_putexternalid)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | The Project ID |
| `externalId` | body | `string` | no | — |
