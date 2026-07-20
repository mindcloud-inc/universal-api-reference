# Batch Update Time Entries with Timing

Updates multiple time entries at once in Timing.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/time-entries/batch-update`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [Batch Update Time Entries](https://web.timingapp.com/docs/#time-entries-PATCHapi-v1-time-entries-batch-update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `time_entries[]` | body | `array<string>` | yes |
| `data` | body | `object` | yes |
