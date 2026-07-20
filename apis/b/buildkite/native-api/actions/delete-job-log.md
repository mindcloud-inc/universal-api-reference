# Delete Job Log with Buildkite

Deletes a job log from Buildkite.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/log`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Delete Job Log](https://buildkite.com/docs/apis/rest-api/jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build` | path | `string` | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `job` | path | `string` | yes | The Buildkite job UUID. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
