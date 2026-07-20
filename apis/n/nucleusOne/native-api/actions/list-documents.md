# List Documents with Nucleus One

Retrieves project documents from Nucleus One.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/documents`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Documents](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `cursor` | query | `string` | no | Pagination cursor |
| `documentFolderId` | query | `string` | no | Filter by folder ID |
| `showAll` | query | `string` | no | If true, returns all results without pagination |
| `documentGroupId` | query | `string` | no | Filter by document group ID |
| `sortType` | query | `string` | no | Sort order for results |
| `unsigned` | query | `string` | no | Filter for unsigned documents |
| `hasSinglePageImages` | query | `string` | no | Filter for documents with single page images |
| `documentOriginType` | query | `string` | no | Filter by document origin type |
