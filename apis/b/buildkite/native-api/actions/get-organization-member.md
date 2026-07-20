# Get Organization Member with Buildkite

Retrieves an organization member from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/members/:user`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Get Organization Member](https://buildkite.com/docs/apis/rest-api/organizations/members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `user` | path | `string` | yes | The Buildkite user ID or slug for the organization member. |
