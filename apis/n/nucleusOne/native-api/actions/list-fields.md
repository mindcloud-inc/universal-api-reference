# List Fields with Nucleus One

Retrieves project fields from Nucleus One.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/fields`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Fields](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `getAll` | query | `string` | no | If true, returns all results without pagination |
| `cursor` | query | `string` | no | Pagination cursor |
