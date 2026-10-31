# Set Account User Permission Group with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/users/:id/membership`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Set Account User Permission Group](https://developers.gobridgit.com/reference/accountusers_setmembership)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | ID of the user to modify |
| `groupingPermissions[]` | body | `array<object>` | yes | — |
| `groupingPermissions[].id` | body | `number` | yes | — |
| `groupingPermissions[].groupId` | body | `number` | yes | — |
| `group` | body | `string` | no | — |
