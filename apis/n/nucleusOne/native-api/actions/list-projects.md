# List Projects with Nucleus One

Retrieves projects from a Nucleus One organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Projects](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `cursor` | query | `string` | no | Pagination cursor |
| `nameFilter` | query | `string` | no | Filter projects by name |
| `getAll` | query | `boolean` | no | Return all projects without pagination |
| `adminOnly` | query | `boolean` | no | Only return projects where user is admin |
| `includeProjectId` | query | `string` | no | Ensure this project ID is included in results |
