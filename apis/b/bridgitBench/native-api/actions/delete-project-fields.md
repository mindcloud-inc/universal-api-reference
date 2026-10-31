# Delete Project Fields with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:id/project-fields`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Project Fields](https://developers.gobridgit.com/reference/projectfields_delete)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Account ID |
| `payload[]` | body | `array<number>` | yes | — |
