# Update Person Groupings with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/groupings`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Person Groupings](https://developers.gobridgit.com/reference/persongroupings_put)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | The person ID |
| `payload[]` | body | `array<number>` | yes | — |
