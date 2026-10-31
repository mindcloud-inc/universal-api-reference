# Delete Project Role with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/roles/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Project Role](https://developers.gobridgit.com/reference/projectroles_remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID that the role belongs to |
| `id` | path | `number` | yes | The role ID |
