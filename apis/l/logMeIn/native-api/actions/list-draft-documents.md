# List Draft Documents with LogMeIn

Retrieves draft knowledge base documents from LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/resolve/knowledge-base/v2/drafts`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [List Draft Documents](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number starting from 1. |
| `pageSize` | query | `number` | no | Number of draft documents per page. |
| `searchText` | query | `string` | no | Search text for draft titles, user names, and labels. |
| `visibilityFilter` | query | `string` | no | Visibility filter. |
| `sort` | query | `string` | no | Sort field, prefix with '-' for descending order. |
| `tenantIds` | query | `string` | no | Comma-separated tenant IDs to filter by. |
