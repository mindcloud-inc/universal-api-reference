# List Recycle Bin Documents with Nucleus One

Retrieves recycle bin documents from a Nucleus One project.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/recycleBinDocuments`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Recycle Bin Documents](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Pagination cursor |
| `organizationId` | path | `string` | yes | organizationId path parameter. |
| `projectId` | path | `string` | yes | projectId path parameter. |
| `projectId` | path | `string` | yes | projectId path parameter. |
