# List Links with Short.io

Retrieves links from Short.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/links`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [List Links](https://developers.short.io/reference/get_api-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | query | `number` | yes | Domain ID. |
| `idString` | query | `string` | no | Link ID string. |
| `folderId` | query | `string` | no | Folder ID. |
| `createdAt` | query | `string` | no | Created-at selector. |
| `beforeDate` | query | `string` | no | Return links created before this timestamp. |
| `afterDate` | query | `string` | no | Return links created after this timestamp. |
| `dateSortOrder` | query | `string` | no | Sort order for link dates. |
| `pageToken` | query | `string` | no | Pagination token from a previous response. |
