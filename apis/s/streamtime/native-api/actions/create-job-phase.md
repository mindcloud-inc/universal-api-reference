# Create Job Phase with Streamtime

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:job_id/job_phases`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Create Job Phase](https://api.streamtime.net/v2/swagger#/Jobs/createJobPhase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `number` | yes | Job ID |
| `name` | body | `string` | yes | Name of the phase |
