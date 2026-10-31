# Delete Person Fields with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:id/person-fields`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Fields](https://developers.gobridgit.com/reference/personfields_delete)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `payload[]` | body | `array<number>` | yes |
