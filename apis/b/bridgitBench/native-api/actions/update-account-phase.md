# Update Account Phase with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/Phases/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Account Phase](https://developers.gobridgit.com/reference/phases_updatesingle)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | The Phase ID |
| `name` | body | `string` | yes | — |
| `includeOnNewProjects` | body | `boolean` | yes | — |
