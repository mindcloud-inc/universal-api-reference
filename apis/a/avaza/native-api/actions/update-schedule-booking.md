# Update Schedule Booking with Avaza

Updates an existing schedule booking in Avaza.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ScheduleSeries/EditBooking`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Update Schedule Booking](https://api.avaza.com/#!/ScheduleSeries/ScheduleSeries_EditBooking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ScheduleSeriesID` | body | `number` | no | — |
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
