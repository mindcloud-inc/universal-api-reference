# Delete Role Names with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/role-names`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Role Names](https://developers.gobridgit.com/reference/rolenames_delete)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID |
| `payload[]` | body | `array<number>` | yes | — |
