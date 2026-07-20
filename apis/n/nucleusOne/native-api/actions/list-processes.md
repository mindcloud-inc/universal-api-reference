# List Processes with Nucleus One

Retrieves project processes from Nucleus One.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/processes`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Processes](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID |
| `projectId` | path | `string` | yes | Project ID |
| `cursor` | query | `string` | no | Pagination cursor. Leave empty to get the first page of results. |
| `getAll` | query | `string` | no | Get all results without pagination |
| `sortDescending` | query | `string` | no | Sort results in descending order |
