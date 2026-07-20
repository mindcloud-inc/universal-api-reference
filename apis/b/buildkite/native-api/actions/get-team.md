# Get Team with Buildkite

Retrieves a team from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/teams/:team`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Get Team](https://buildkite.com/docs/apis/rest-api/teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `team` | path | `string` | yes | The Buildkite team slug. |
