# Schedule Email with Benchmark Email

Schedules an email in Benchmark Email.

## Endpoint

- **Method:** `POST`
- **Path:** `/Emails/:id/Schedule`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [Schedule Email](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Benchmark email ID. |
| `ListID` | body | `string` | no | Optional resend target list ID. |
| `ScheduleDate` | body | `string` | yes | Scheduled send datetime. |
| `SendType` | body | `string` | no | Optional resend send type. |
| `TimeZone` | body | `string` | yes | Timezone for the scheduled send. |
