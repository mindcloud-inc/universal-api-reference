# Create Multiple Logged Time Entries with Streamtime

## Endpoint

- **Method:** `POST`
- **Path:** `/logged_times/bulk`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Create Multiple Logged Time Entries](https://api.streamtime.net/v2/swagger#/ToDos/createLoggedTimeBulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `loggedTimes[]` | body | `array<object>` | yes | Array of logged time entry payloads. |
