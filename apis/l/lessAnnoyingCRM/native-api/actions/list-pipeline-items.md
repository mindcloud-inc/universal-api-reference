# List Pipeline Items with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [List Pipeline Items](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Pipeline_Items#Goto-GetPipelineItems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PipelineId` | body | `string` | yes | The pipeline Id to search within. |
| `UserFilter` | body | `string` | no | JSON array of UserIds to filter by related contact owner. |
| `StatusFilter` | body | `string` | no | JSON array of StatusIds to restrict the result set. |
| `AdvancedFilters` | body | `string` | no | JSON array of advanced pipeline filter objects. |
| `SortBy` | body | `string` | no | Field used for sorting. |
| `SortDirection` | body | `string` | no | Ascending or Descending sort order. |
| `MaxNumberOfResults` | body | `number` | no | Maximum number of results to return. |
| `Page` | body | `number` | no | Pagination page number starting at 1. |
