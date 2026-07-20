# List Notes with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [List Notes](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Notes#Goto-GetNotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SortDirection` | body | `string` | no | Ascending or Descending note order by date. |
| `DateFilterStart` | body | `date` | no | Only return notes on or after this date/time. |
| `DateFilterEnd` | body | `date` | no | Only return notes on or before this date/time. |
| `UserFilter` | body | `string` | no | JSON array of UserIds to filter by author. |
| `ContactId` | body | `string` | no | Only return notes attached to this contact. |
| `MaxNumberOfResults` | body | `number` | no | Maximum number of results to return. |
| `Page` | body | `number` | no | Pagination page number starting at 1. |
