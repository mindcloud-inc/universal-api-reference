# List Team Members with Buildkite

Retrieves team members from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/teams/:team/members`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Team Members](https://buildkite.com/docs/apis/rest-api/teams/members)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `team` | path | `string` | yes | The Buildkite team slug. |
