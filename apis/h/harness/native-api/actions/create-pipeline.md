# Create Pipeline with Harness

Creates a new pipeline in Harness.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.harness.io/pipeline/api/pipelines/v2?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [Create Pipeline](https://apidocs.harness.io/pipelines/create-pipeline)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/yaml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Pipeline description. |
| `identifier` | body | `string` | yes | Pipeline identifier. |
| `name` | body | `string` | yes | Pipeline display name. |
