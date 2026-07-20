# List Organization Builds with Buildkite

Retrieves organization builds from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/builds`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Organization Builds](https://buildkite.com/docs/apis/rest-api/builds)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
