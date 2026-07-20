# Search Contacts with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Search Contacts](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Contacts#Goto-GetContacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SearchTerms` | body | `string` | no | Values to search for in record fields. |
| `RequiresWriteAccess` | body | `boolean` | no | Only return contacts the connected user can edit. |
| `RecordTypeFilter` | body | `string` | no | Limit results to Contacts or Companies. |
| `OwnerFilter` | body | `string` | no | JSON array of UserIds to filter assigned contacts. |
| `SortBy` | body | `string` | no | Field used for sorting. |
| `SortDirection` | body | `string` | no | Ascending or Descending sort order. |
| `AdvancedFilters` | body | `string` | no | JSON array of advanced filter objects. |
| `MaxNumberOfResults` | body | `number` | no | Maximum number of results to return. |
| `Page` | body | `number` | no | Pagination page number starting at 1. |
