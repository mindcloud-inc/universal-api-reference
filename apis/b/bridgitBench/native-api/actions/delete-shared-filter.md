# Delete Shared Filter with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/shared-filters/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Shared Filter](https://developers.gobridgit.com/reference/sharedfilters_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `string` | yes | Id of the filter to remove |
