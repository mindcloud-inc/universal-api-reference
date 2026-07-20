# List Deleted Timesheets with Avaza

Retrieves deleted timesheet entries from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Timesheet/deleted`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Deleted Timesheets](https://api.avaza.com/#!/Timesheet/Timesheet_GetDeletedTimesheets)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UserID` | query | `number` | no | Filter by user ID |
| `DeletedAfter` | query | `date` | no | Filter entries deleted after this UTC date |
| `EntryDateFrom` | query | `date` | no | Filter by original timesheet entry date (start) |
| `EntryDateTo` | query | `date` | no | Filter by original timesheet entry date (end) |
| `PageSize` | query | `number` | no | Number of items per page |
| `PageNumber` | query | `number` | no | Page number (starts from 1) |
