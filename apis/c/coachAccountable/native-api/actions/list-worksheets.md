# List Worksheets with CoachAccountable

Retrieves worksheets from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Worksheets](https://www.coachaccountable.com/APIDocs#Worksheet.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | Filter Worksheets by Client. |
| `CompanyID` | body | `number` | no | Filter Client Worksheets by which Company they belong to. |
| `title` | body | `string` | no | Filter a Client's Worksheets by which title, prefixed. |
| `includeContent` | body | `boolean` | no | Set to true to include the full HTML content of the Worksheet. |
| `includeOutstanding` | body | `boolean` | no | Set to true to include Worksheets not yet marked complete. |
| `dateAssignedFrom` | body | `date` | no | Set to filter Worksheet by when they were assigned. |
| `dateAssignedTo` | body | `date` | no | Set to filter Worksheet by when they were assigned. |
| `sortField` | body | `list` | no | Accepted values: `dateAssigned`, `dateDone`, `dateDue`. |
| `sortDirection` | body | `list` | no | Accepted values: `A`, `D`. |
