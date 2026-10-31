# Delete Project Grouping with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/groupings/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Project Grouping](https://developers.gobridgit.com/reference/projectgroupings_remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The Project ID |
| `id` | path | `number` | yes | The grouping ID for project |
