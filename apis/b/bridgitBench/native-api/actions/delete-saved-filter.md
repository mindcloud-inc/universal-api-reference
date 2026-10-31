# Delete Saved Filter with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/my-filters/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Saved Filter](https://developers.gobridgit.com/reference/userfilters_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the filter to remove |
