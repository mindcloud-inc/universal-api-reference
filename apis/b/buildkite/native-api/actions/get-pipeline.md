# Get Pipeline with Buildkite

Retrieves a pipeline from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/pipelines/:pipeline`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Get Pipeline](https://buildkite.com/docs/apis/rest-api/pipelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
