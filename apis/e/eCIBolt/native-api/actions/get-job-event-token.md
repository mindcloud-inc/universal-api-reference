# Get Job Event Token with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/jobs/events/at`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [Get Job Event Token](https://app.bolttech.net/api-docs/index.html#/Jobs/get_open_v1_jobs_events_at)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `date` | yes | Start date and time for the change history. Bolt receives an ISO 8601 timestamp. |
