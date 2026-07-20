# Download Artifact with Buildkite

Downloads an artifact from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/artifacts/:artifact/download`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Download Artifact](https://buildkite.com/docs/apis/rest-api/artifacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `artifact` | path | `string` | yes | The Buildkite artifact UUID. |
| `build` | path | `string` | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `job` | path | `string` | yes | The Buildkite job UUID. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
