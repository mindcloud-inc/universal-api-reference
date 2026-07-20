# Create Input Set with Harness

Creates a new input set in Harness.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.harness.io/pipeline/api/inputSets?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier&pipelineIdentifier=:pipelineIdentifier`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [Create Input Set](https://apidocs.harness.io/input-sets/create-input-set)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/yaml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | body | `string` | yes | Input set identifier. |
| `message` | body | `string` | yes | Approval message runtime value. |
| `name` | body | `string` | yes | Input set display name. |
| `pipelineIdentifier` | path | `string` | yes | Pipeline identifier. |
