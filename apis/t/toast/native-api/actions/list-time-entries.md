# List Time Entries with Toast

Retrieves employee time entries using identifiers, date ranges, modification ranges, or business date.

## Endpoint

- **Method:** `GET`
- **Path:** `/labor/v1/timeEntries`
- **Base URL:** `{connection}`
- **API:** Labor
- **Official documentation:** [List Time Entries](https://doc.toasttab.com/openapi/labor/operation/timeEntriesGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeEntryIds` | query | `string` | no | One or more Toast GUIDs or external time-entry identifiers, with a maximum of 100. Send multiple values as a array. |
| `startDate` | query | `date` | no | Inclusive clock-in beginning of the time-entry range in ISO-8601 format. |
| `endDate` | query | `date` | no | Exclusive clock-in end of the time-entry range in ISO-8601 format. |
| `modifiedStartDate` | query | `date` | no | Inclusive beginning of the modification range in ISO-8601 format. |
| `modifiedEndDate` | query | `date` | no | Exclusive end of the modification range in ISO-8601 format. |
| `businessDate` | query | `date` | no | Restaurant business date in yyyyMMdd format. |
| `includeMissedBreaks` | query | `boolean` | no | Include missed breaks in each time entry break array. |
| `includeArchived` | query | `boolean` | no | Include archived time entries when selecting by start and end date. |
