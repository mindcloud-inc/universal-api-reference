# List Events with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [List Events](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Events#Goto-GetEvents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SortDirection` | body | `string` | no | Ascending or Descending event order. |
| `StartDate` | body | `date` | no | Lower bound of event dates to fetch. |
| `EndDate` | body | `date` | no | Upper bound of event dates to fetch. |
| `UserFilter` | body | `string` | no | JSON array of UserIds to filter attendee calendars. |
| `CalendarFilter` | body | `string` | no | JSON array of CalendarIds to filter by calendar. |
| `ContactId` | body | `string` | no | Only return events attached to this contact. |
| `MaxNumberOfResults` | body | `number` | no | Maximum number of results to return. |
| `Page` | body | `number` | no | Pagination page number starting at 1. |
