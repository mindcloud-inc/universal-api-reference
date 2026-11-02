# List Timesheet Entries with BambooHR

Lists timesheet entries from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time_tracking/timesheet_entries`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Timesheet Entries](https://documentation.bamboohr.com/reference/list-timesheet-entries)

## Requirements

- **OAuth scopes:** `time_tracking`
- **scope:** `time_tracking` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `date` | yes | YYYY-MM-DD. Only show timesheet entries on/after the specified start date. Must be within the last 365 days. Format: `YYYY-MM-DD`. |
| `end` | query | `date` | yes | YYYY-MM-DD. Only show timesheet entries on/before the specified end date. Must be within the last 365 days. Format: `YYYY-MM-DD`. |
| `employeeIds` | query | `string` | no | A comma-separated list of internal employee IDs. When specified, only entries that match these employee IDs are returned. When omitted, entries for all accessible employees are returned. Send multiple values as a string separated by `,`. |
