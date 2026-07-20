# List Documents with LogMeIn

Retrieves knowledge base documents from LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/resolve/knowledge-base/v2/documents`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [List Documents](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number starting from 1. |
| `pageSize` | query | `number` | no | Number of documents per page. |
| `searchText` | query | `string` | no | Search text for document titles, user names, and labels. |
| `visibilityFilter` | query | `string` | no | Visibility filter. |
| `sort` | query | `string` | no | Sort field, prefix with '-' for descending order. |
| `folderId` | query | `string` | no | Folder ID to filter by, or 'none' for documents without a folder. |
| `tenantIds` | query | `string` | no | Comma-separated tenant IDs to filter by. |
