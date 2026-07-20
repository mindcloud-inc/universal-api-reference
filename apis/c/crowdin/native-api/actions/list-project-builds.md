# List Project Builds with Crowdin

Retrieves project builds from Crowdin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/translations/builds`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [List Project Builds](https://support.crowdin.com/developer/api/v2/#operation/api.projects.translations.builds.getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `branchId` | query | `number` | no |
