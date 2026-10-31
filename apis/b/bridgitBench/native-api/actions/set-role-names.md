# Set Role Names with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/role-names`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Set Role Names](https://developers.gobridgit.com/reference/rolenames_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID |
| `alphabetize` | query | `boolean` | no | Optional flag to set whether role names should be alphabetically ordered by the caller |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].id` | body | `number` | yes | — |
| `payload[].name` | body | `string` | yes | — |
| `payload[].cost` | body | `number` | no | — |
| `payload[].isHidden` | body | `boolean` | no | — |
