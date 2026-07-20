# Delete Input Set with Harness

Deletes an input set from Harness.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://app.harness.io/pipeline/api/inputSets/:inputSetIdentifier?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier&pipelineIdentifier=:pipelineIdentifier`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [Delete Input Set](https://apidocs.harness.io/input-sets/delete-input-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputSetIdentifier` | path | `string` | yes | Input set identifier. |
| `pipelineIdentifier` | path | `string` | yes | Pipeline identifier. |
