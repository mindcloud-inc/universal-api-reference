# Search Project Documents with Nucleus One

Finds project documents in Nucleus One by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/searchResults`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [Search Project Documents](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `cursor` | query | `string` | no | Pagination cursor |
| `parentId` | query | `string` | no | Parent ID for hierarchical search |
