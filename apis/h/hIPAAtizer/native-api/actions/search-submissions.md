# Search Submissions with HIPAAtizer

Finds submissions in HIPAAtizer by workflow and search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/api_key/submissions/search`
- **Base URL:** `https://app.hipaatizer.com`
- **Official documentation:** [Search Submissions](https://github.com/HIPAAtizer/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Optional raw request wrapper. Use `{}` for body when only `workflowId` is provided. |
| `request.additionalColumns` | body | `list<string>` | no | Additional columns to include. |
| `request.dates.from` | body | `string` | no | Start date filter. |
| `request.dates.to` | body | `string` | no | End date filter. |
| `request.includeNotCompleted` | body | `boolean` | no | Include incomplete submissions. |
| `request.pagination.limit` | body | `number` | no | Pagination page size. |
| `request.pagination.page` | body | `number` | no | Pagination page number. |
| `request.searchBy` | body | `string` | no | Field used for search. |
| `request.searchById` | body | `string` | no | ID used for search. |
| `request.searchFor` | body | `string` | no | Search term value. |
| `request.sorting.additionalColumn` | body | `string` | no | Additional sorting column. |
| `request.sorting.column` | body | `string` | no | Primary sorting column. |
| `request.sorting.direction` | body | `string` | no | Sort direction. |
| `workflowId` | query | `string` | yes | Workflow UUID to scope submission search. |
