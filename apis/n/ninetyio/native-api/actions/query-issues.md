# Query Issues with Ninety.io

Retrieves issues from Ninety.io with optional team and interval filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/issues/query`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Query Issues](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sortField` | body | `string` | no | The field to sort results by |
| `sortDirection` | body | `string` | no | The sort direction |
| `pageSize` | body | `number` | no | Number of items per page |
| `pageIndex` | body | `number` | no | Zero-based page index |
| `teamId` | body | `string` | no | A single team Id or a comma-separated list of team Ids to filter by |
| `intervalCode` | body | `string` | no | Filter by Issue classification |
| `searchText` | body | `string` | no | Search text to match against Issue title, description, and comments |
