# Update Permission with Documently

Updates an existing permission in Documently.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/permissions/:permissionId`
- **Base URL:** `https://app.documently.io/api`
- **Official documentation:** [Update Permission](https://app.documently.io/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `permissionId` | path | `string` | no | Permission ID. |
| `role` | body | `string` | no | Permission role. |
