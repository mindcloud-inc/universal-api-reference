# Get Team Member with Buildkite

Retrieves a team member from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/teams/:team/members/:user`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Get Team Member](https://buildkite.com/docs/apis/rest-api/teams/members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `team` | path | `string` | yes | The Buildkite team slug. |
| `user` | path | `string` | yes | The Buildkite user ID or slug for the team member. |
