# Get Timesheet Totals with Connecteam

Retrieves detailed work records for each employee within a specified date range. This endpoint is designed to support payroll processing by providing total worked hours, categorized by pay rules and resource (if applied in the account settings). Ideal for integrating with external payroll systems to ensure accurate information. The pay rate will be presented in case it is defined within the account. If an automated unpaid break is applied, it will  be deducted from the total hours value. In order to retrieve approved paid time-off (PTO) and manual break information, please use the Get time activities endpoint. Hours will be presented in decimal format. The time period is limited to 45 days.

## Endpoint

- **Method:** `GET`
- **Path:** `/time-clock/v1/time-clocks/:timeClockId/timesheet`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Get Timesheet Totals](https://developer.connecteam.com/reference/get_timesheet_total_hours_time_clock_v1_time_clocks__timeClockId__timesheet_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeClockId` | path | `number` | yes | — |
| `startDate` | query | `string` | yes | — |
| `endDate` | query | `string` | yes | — |
| `userIds` | query | `array<number>` | no | Send multiple values as a array. |
| `groupIds` | query | `array<string>` | no | Send multiple values as a array. |
| `jobIds` | query | `array<string>` | no | Send multiple values as a array. |
| `isApproved` | query | `boolean` | no | — |
| `isSubmitted` | query | `boolean` | no | — |
| `isLocked` | query | `boolean` | no | — |
