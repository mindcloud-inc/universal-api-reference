# Get Job Run with Databricks

Retrieves a job run from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.2/jobs/runs/get`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Get Job Run](https://docs.databricks.com/api/workspace/jobs/getrun)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | query | `number` | yes | The canonical identifier of the run for which to retrieve the metadata. This field is required. |
| `include_history` | query | `boolean` | no | Whether to include the repair history in the response. |
| `include_resolved_values` | query | `boolean` | no | Whether to include resolved parameter values in the response. |
| `page_token` | query | `string` | no | Use `next_page_token` returned from the previous GetRun response to request the next page of the run's array properties. |
