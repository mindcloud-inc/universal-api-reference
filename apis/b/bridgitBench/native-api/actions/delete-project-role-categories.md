# Delete Project Role Categories with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/role-categories`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Project Role Categories](https://developers.gobridgit.com/reference/projectrolecategories_remove)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID to delete the categories from |
| `payload[]` | body | `array<number>` | yes | — |
