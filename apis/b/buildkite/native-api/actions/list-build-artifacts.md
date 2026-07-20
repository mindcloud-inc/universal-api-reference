# List Build Artifacts with Buildkite

Retrieves build artifacts from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds/:build/artifacts`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Build Artifacts](https://buildkite.com/docs/apis/rest-api/artifacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build` | path | `string` | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
