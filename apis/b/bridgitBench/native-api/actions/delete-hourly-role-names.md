# Delete Hourly Role Names with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:id/hourly-role-names`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Hourly Role Names](https://developers.gobridgit.com/reference/hourlyrolenames_delete)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The account ID |
| `payload[]` | body | `array<number>` | yes | — |
