# List Job Events with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/jobs/events`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [List Job Events](https://app.bolttech.net/api-docs/index.html#/Jobs/get_open_v1_jobs_events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_token` | query | `string` | yes | Token used to get the next list of events. |
