# Update Account Grouping with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/groupings/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Account Grouping](https://developers.gobridgit.com/reference/accountgroupings_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the grouping to update |
| `name` | body | `string` | yes | — |
