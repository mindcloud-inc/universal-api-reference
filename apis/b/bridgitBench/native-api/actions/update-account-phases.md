# Update Account Phases with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/Phases`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Account Phases](https://developers.gobridgit.com/reference/phases_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].id` | body | `number` | yes | — |
| `payload[].name` | body | `string` | yes | — |
| `payload[].includeOnNewProjects` | body | `boolean` | yes | — |
