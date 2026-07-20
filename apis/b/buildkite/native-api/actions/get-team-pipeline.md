# Get Team Pipeline with Buildkite

Retrieves a team pipeline from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/teams/:team/pipelines/:pipeline`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Get Team Pipeline](https://buildkite.com/docs/apis/rest-api/teams/pipelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
| `team` | path | `string` | yes | The Buildkite team slug. |
