# List Jobs with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/jobs`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [List Jobs](https://app.bolttech.net/api-docs/index.html#/Jobs/get_open_v1_jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | query | `string` | no | Token used to get the changed jobs, returned on the last page of the jobs. You should only send the refresh_token or the next_batch. |
| `refresh` | query | `string` | no | Return only directly changed records when value is "self" |
