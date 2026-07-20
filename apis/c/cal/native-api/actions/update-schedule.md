# Update Schedule with Cal.com

Updates a schedule in Cal.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/schedules/:scheduleId`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Update Schedule](https://cal.com/docs/api-reference/v2/schedules/update-a-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduleId` | path | `list` | yes | Schedule identifier from Cal.com path parameter. |
| `name` | body | `string` | no | Updated schedule name. |
| `timeZone` | body | `string` | no | Updated IANA time zone for the schedule. |
| `isDefault` | body | `boolean` | no | Set true to make this the default schedule. |
| `availability[]` | body | `array<object>` | no | Availability windows for recurring weekly schedule blocks. |
| `availability[].days[]` | body | `array<string>` | no | Weekday list for an availability window. |
| `availability[].startTime` | body | `string` | no | Start time for an availability window. |
| `availability[].endTime` | body | `string` | no | End time for an availability window. |
| `overrides[]` | body | `array<object>` | no | Date-specific availability overrides. |
| `overrides[].date` | body | `string` | no | Override date in ISO date format. |
| `overrides[].startTime` | body | `string` | no | Start time for an override window. |
| `overrides[].endTime` | body | `string` | no | End time for an override window. |
