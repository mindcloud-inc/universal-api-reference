# Delete Account Phases with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/Phases`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Account Phases](https://developers.gobridgit.com/reference/phases_delete)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `payload[]` | body | `array<number>` | yes | — |
