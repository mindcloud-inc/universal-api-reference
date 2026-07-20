# List Pipelines with Buildkite

Retrieves pipelines from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/pipelines`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Pipelines](https://buildkite.com/docs/apis/rest-api/pipelines)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
