# List Document Folders with Nucleus One

Retrieves document folders from a Nucleus One project.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/documentFolders`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Document Folders](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
