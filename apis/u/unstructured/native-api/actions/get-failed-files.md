# Get Failed Files with Unstructured

Retrieves failed files for a job from Unstructured.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:job_id/failed-files`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Get Failed Files](https://docs.unstructured.io/api-reference/jobs/get-failed-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The job ID. |
