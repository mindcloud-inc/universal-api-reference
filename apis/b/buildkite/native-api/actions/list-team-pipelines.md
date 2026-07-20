# List Team Pipelines with Buildkite

Retrieves team pipelines from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/teams/:team/pipelines`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Team Pipelines](https://buildkite.com/docs/apis/rest-api/teams/pipelines)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `team` | path | `string` | yes | The Buildkite team slug. |
