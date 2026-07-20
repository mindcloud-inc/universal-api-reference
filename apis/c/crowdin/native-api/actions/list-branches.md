# List Branches with Crowdin

Retrieves branches from a Crowdin project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/branches`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [List Branches](https://support.crowdin.com/developer/api/v2/#operation/api.projects.branches.getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `orderBy` | query | `string` | no |
| `name` | query | `string` | no |
