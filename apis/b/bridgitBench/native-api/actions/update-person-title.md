# Update Person Title with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/titles/:entryId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Person Title](https://developers.gobridgit.com/reference/persontitles_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | Id of the person the entry belongs to |
| `entryId` | path | `number` | yes | Id of the title entry to update |
| `payload` | body | `object` | no | — |
