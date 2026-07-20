# Update Job Status with Streamtime

## Endpoint

- **Method:** `PUT`
- **Path:** `/jobs/:job_id/job_status`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Update Job Status](https://api.streamtime.net/v2/swagger#/Jobs/updateJobStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `number` | yes | Job ID |
| `job_status_id` | query | `number` | yes | Job Status ID (5=Paused, 1=In Play, 2=Done, 3=Deleted, 4=Archived) |
