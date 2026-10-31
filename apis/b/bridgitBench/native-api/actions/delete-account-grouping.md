# Delete Account Grouping with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/groupings/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Account Grouping](https://developers.gobridgit.com/reference/accountgroupings_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the grouping to remove |
