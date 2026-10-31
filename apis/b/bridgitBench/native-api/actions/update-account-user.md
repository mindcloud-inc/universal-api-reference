# Update Account User with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/users/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Account User](https://developers.gobridgit.com/reference/accountusers_patch)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the user to update |
| `name` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `phoneNumber` | body | `string` | no | — |
| `team` | body | `string` | no | — |
