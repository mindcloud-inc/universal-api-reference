# Update Branch with Documently

Updates an existing branch in Documently.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/branches/:branchId`
- **Base URL:** `https://app.documently.io/api`
- **Official documentation:** [Update Branch](https://app.documently.io/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `branchId` | path | `string` | yes |
| `name` | body | `string` | yes |
| `project` | body | `string` | yes |
| `status` | body | `string` | yes |
