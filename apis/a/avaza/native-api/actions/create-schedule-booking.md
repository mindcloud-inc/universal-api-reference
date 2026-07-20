# Create Schedule Booking with Avaza

Creates a project work booking in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/ScheduleSeries/AddBooking`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Schedule Booking](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_AddBooking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UserIDFK` | body | `number` | no | — |
| `HoursPerDay` | body | `number` | no | — |
| `TotalDuration` | body | `number` | no | — |
| `DurationType` | body | `string` | no | Possible values are "HoursPerDay" or "TotalDuration" |
| `ScheduleOnDaysOff` | body | `boolean` | no | — |
| `ProjectIDFK` | body | `number` | no | — |
| `CategoryIDFK` | body | `number` | no | — |
| `TaskIDFK` | body | `number` | no | — |
| `Notes` | body | `string` | no | — |
| `StartDate` | body | `date` | no | — |
| `EndDate` | body | `date` | no | — |
| `StartTime` | body | `string` | no | — |
