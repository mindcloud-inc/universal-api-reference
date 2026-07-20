# Update Pay Schedule with Aspire

Updates an existing pay schedule in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `PaySchedules`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Pay Schedule](https://cloud-api.youraspire.com/swagger/index.html#/PaySchedules/PaySchedules_Update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PayScheduleName` | body | `string` | yes |
| `DailyHoursBeforeOT` | body | `number` | yes |
| `WeeklyHoursBeforeOT` | body | `number` | yes |
| `Active` | body | `boolean` | yes |
| `DefaultOTPayCodeID` | body | `number` | yes |
| `DefaultPayCodeID` | body | `number` | yes |
| `PayScheduleID` | body | `number` | yes |
