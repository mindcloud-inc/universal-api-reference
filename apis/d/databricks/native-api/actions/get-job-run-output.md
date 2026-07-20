# Get Job Run Output with Databricks

Retrieves output for a Databricks job run.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.2/jobs/runs/get-output`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Get Job Run Output](https://docs.databricks.com/api/workspace/jobs/getrunoutput)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | query | `number` | yes | The canonical identifier for the run. |
