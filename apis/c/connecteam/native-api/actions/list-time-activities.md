# List Time Activities with Connecteam

Retrieve a list of time activities in under a specified time clock.
Time activities include shift and/or manual breaks

## Endpoint

- **Method:** `GET`
- **Path:** `/time-clock/v1/time-clocks/:timeClockId/time-activities`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [List Time Activities](https://developer.connecteam.com/reference/get_time_activities_time_clock_v1_time_clocks__timeClockId__time_activities_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeClockId` | path | `number` | yes | — |
| `startDate` | query | `string` | yes | — |
| `endDate` | query | `string` | yes | — |
| `userIds` | query | `array<number>` | no | Send multiple values as a array. |
| `jobIds` | query | `array<string>` | no | Send multiple values as a array. |
| `manualBreakIds` | query | `array<string>` | no | Send multiple values as a array. |
| `policyTypeIds` | query | `array<string>` | no | Send multiple values as a array. |
| `activityTypes` | query | `array<string>` | no | Send multiple values as a array. |
