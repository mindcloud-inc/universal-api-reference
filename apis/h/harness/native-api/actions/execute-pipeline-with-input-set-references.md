# Execute Pipeline With Input Set References with Harness

Executes a Harness pipeline with input set references.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.harness.io/pipeline/api/pipeline/execute/:pipelineIdentifier/inputSetList?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [Execute Pipeline With Input Set References](https://apidocs.harness.io/pipeline-execution/postpipelineexecutewithinputsetyaml)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputSetIdentifier` | body | `string` | yes | Referenced input set identifier. |
| `pipelineIdentifier` | path | `string` | yes | Pipeline identifier. |
