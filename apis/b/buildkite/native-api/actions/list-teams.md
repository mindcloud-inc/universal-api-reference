# List Teams with Buildkite

Retrieves teams from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/teams`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Teams](https://buildkite.com/docs/apis/rest-api/teams)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
