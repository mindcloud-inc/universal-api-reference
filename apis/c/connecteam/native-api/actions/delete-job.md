# Delete Job with Connecteam

Delete a single job by its unique identifier.
        Currently, deleting a sub-job and/or job with nested sub-jobs is not supported.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/jobs/v1/jobs/:jobId`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Delete Job](https://developer.connecteam.com/reference/delete_job_jobs_v1_jobs__jobId__delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `jobId` | path | `string` | yes |
