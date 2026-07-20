# Get Job with Databricks

Retrieves a job from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.2/jobs/get`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Get Job](https://docs.databricks.com/api/workspace/jobs/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | query | `number` | yes | The canonical identifier of the job to retrieve information about. This field is required. |
| `page_token` | query | `string` | no | Use `next_page_token` returned from the previous GetJob response to request the next page of the job's array properties. |
