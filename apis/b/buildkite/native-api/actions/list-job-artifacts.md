# List Job Artifacts with Buildkite

Retrieves job artifacts from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/artifacts`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Job Artifacts](https://buildkite.com/docs/apis/rest-api/artifacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build` | path | `string` | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `job` | path | `string` | yes | The Buildkite job UUID. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
