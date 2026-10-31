# Delete Person Unavailabilities with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:id/unavailabilities`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Unavailabilities](https://developers.gobridgit.com/reference/personunavailabilities_deleteunavailabilities)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the person to get unavailabilities for |
| `payload[]` | body | `array<number>` | yes | — |
