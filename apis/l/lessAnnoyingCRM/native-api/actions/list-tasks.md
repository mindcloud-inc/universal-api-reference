# List Tasks with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [List Tasks](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Tasks#Goto-GetTasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `StartDate` | body | `date` | yes | Lower bound of dates to fetch. |
| `EndDate` | body | `date` | yes | Upper bound of dates to fetch. |
| `UserFilter` | body | `string` | no | JSON array of UserIds to filter assignees. |
| `ContactId` | body | `string` | no | Only return tasks attached to this contact. |
| `CompletionStatus` | body | `string` | no | Both, Incomplete, or Complete. |
| `SortDirection` | body | `string` | no | Ascending or Descending sort order. |
| `MaxNumberOfResults` | body | `number` | no | Maximum number of results to return. |
| `Page` | body | `number` | no | Pagination page number starting at 1. |
