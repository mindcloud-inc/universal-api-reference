# List Tags with Nucleus One

Retrieves project tags from Nucleus One.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/tags`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Tags](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `cursor` | query | `string` | no | Pagination cursor. Leave empty to get the first page of results. |
