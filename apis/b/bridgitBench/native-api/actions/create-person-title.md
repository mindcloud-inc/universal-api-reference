# Create Person Title with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/titles`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Person Title](https://developers.gobridgit.com/reference/persontitles_add)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | Id of the person to add the entry to |
| `titleValueId` | body | `number` | no | The account title list value to record; mutually exclusive with `title`. |
| `title` | body | `string` | no | A freeform title; mutually exclusive with `titleValueId`. |
| `startDate` | body | `date` | yes | — |
| `endDate` | body | `date` | yes | — |
