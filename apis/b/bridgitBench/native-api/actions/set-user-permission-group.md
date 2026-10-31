# Set User Permission Group with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/Users/:id/membership`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Set User Permission Group](https://developers.gobridgit.com/reference/users_setmembership)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Id of the user to remove |
| `group` | body | `string` | no | — |
