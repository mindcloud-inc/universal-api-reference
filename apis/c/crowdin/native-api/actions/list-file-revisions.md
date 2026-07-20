# List File Revisions with Crowdin

Retrieves file revisions from a Crowdin project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/files/:fileId/revisions`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [List File Revisions](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.revisions.getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `fileId` | path | `number` | yes |
