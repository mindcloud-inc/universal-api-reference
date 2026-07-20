# Get Time Entry with FreshBooks

Retrieves a time entry from FreshBooks for a business.

## Endpoint

- **Method:** `GET`
- **Path:** `/timetracking/business/:businessId/time_entries/:timeEntryId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Get Time Entry](https://www.freshbooks.com/api/time_entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | FreshBooks business ID. |
| `timeEntryId` | path | `string` | yes | FreshBooks time entry ID. |
