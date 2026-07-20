# List Applications By Job with CATS

Retrieves applications for a job in CATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:job_id/applications`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [List Applications By Job](https://docs.catsone.com/api/v3/#jobs-list-applications-by-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `number` | yes | The ID of the job to return applications for. |
