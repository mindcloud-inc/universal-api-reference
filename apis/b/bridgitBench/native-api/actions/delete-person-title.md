# Delete Person Title with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/titles/:entryId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Title](https://developers.gobridgit.com/reference/persontitles_remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | Id of the person the entry belongs to |
| `entryId` | path | `number` | yes | Id of the title entry to remove |
