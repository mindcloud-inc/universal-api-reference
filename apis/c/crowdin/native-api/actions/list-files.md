# List Files with Crowdin

Retrieves files from a Crowdin project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/files`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [List Files](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `orderBy` | query | `string` | no |
| `branchId` | query | `number` | no |
| `directoryId` | query | `number` | no |
| `filter` | query | `string` | no |
| `recursion` | query | `number` | no |
