# Set Person Profile Picture with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/profile-picture`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Set Person Profile Picture](https://developers.gobridgit.com/reference/personprofile_put)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The unique identifier of the account |
| `personId` | path | `number` | yes | The unique identifier of the person |
| `ImageUrl` | body | `string` | no | — |
