# Get Pipeline with Databricks

Retrieves a pipeline from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.0/pipelines/:pipelineId`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Get Pipeline](https://docs.databricks.com/api/workspace/pipelines/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pipeline_id` | path | `string` | yes |
