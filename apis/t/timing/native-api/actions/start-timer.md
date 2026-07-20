# Start Timer with Timing

Starts a new timer in Timing, stopping any running timer.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-entries/start`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [Start Timer](https://web.timingapp.com/docs/#time-entries-POSTapi-v1-time-entries-start)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project` | body | `string` | no |
| `title` | body | `string` | no |
