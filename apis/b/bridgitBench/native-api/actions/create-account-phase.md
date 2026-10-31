# Create Account Phase with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/Phases`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Account Phase](https://developers.gobridgit.com/reference/phases_add)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `name` | body | `string` | yes | — |
| `includeOnNewProjects` | body | `boolean` | yes | — |
