# List Pipeline Builds with Buildkite

Retrieves pipeline builds from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Pipeline Builds](https://buildkite.com/docs/apis/rest-api/builds)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
