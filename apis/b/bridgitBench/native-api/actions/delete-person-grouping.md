# Delete Person Grouping with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/groupings/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Grouping](https://developers.gobridgit.com/reference/persongroupings_remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | The person ID |
| `id` | path | `number` | yes | The grouping ID for person |
