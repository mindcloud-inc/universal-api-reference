# List Form Templates with Nucleus One

Retrieves form templates from a Nucleus One project.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/formTemplates`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Form Templates](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `cursor` | query | `string` | no | Pagination cursor. Leave empty to get the first page of results. |
| `pageSize` | query | `number` | no | Number of items per page |
