# List Project Role Categories with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/role-categories`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Project Role Categories](https://developers.gobridgit.com/reference/projectrolecategories_query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID to get categories from |
