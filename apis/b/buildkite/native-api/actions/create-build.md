# Create Build with Buildkite

Creates a new build in Buildkite.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Create Build](https://buildkite.com/docs/apis/rest-api/builds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | body | `string` | yes | The branch name for the new build. |
| `commit` | body | `string` | yes | The commit SHA to build. |
| `message` | body | `string` | no | An optional message for the new build. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
