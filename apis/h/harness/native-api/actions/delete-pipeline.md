# Delete Pipeline with Harness

Deletes a pipeline from Harness.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://app.harness.io/pipeline/api/pipelines/:pipelineIdentifier?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [Delete Pipeline](https://apidocs.harness.io/pipelines/delete-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineIdentifier` | path | `string` | yes | Pipeline identifier. |
