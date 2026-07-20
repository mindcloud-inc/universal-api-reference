# List Project Members with Nucleus One

Retrieves project members from Nucleus One.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/members`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Project Members](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Pagination cursor. Leave empty to get the first page of results. |
| `organizationId` | path | `string` | yes | organizationId path parameter. |
| `getAll` | query | `string` | no | If true, returns all results without pagination. |
| `projectId` | path | `string` | yes | projectId path parameter. |
