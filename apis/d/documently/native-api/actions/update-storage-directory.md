# Update Storage Directory with Documently

Updates an existing storage directory in Documently.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/storage-directories/:directoryId`
- **Base URL:** `https://app.documently.io/api`
- **Official documentation:** [Update Storage Directory](https://app.documently.io/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `directoryId` | path | `string` | no | The storage directory id. |
| `name` | body | `string` | no | Directory name. |
| `project` | body | `string` | no | Project ID for the directory. |
