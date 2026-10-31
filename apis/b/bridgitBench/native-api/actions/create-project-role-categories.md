# Create Project Role Categories with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/role-categories`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Role Categories](https://developers.gobridgit.com/reference/projectrolecategories_add)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID to add the category to |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].name` | body | `string` | yes | — |
