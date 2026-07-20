# Reprioritize Job with Buildkite

Reprioritizes an existing job in Buildkite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds/:build/jobs/:job/reprioritize`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Reprioritize Job](https://buildkite.com/docs/apis/rest-api/jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build` | path | `string` | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `job` | path | `string` | yes | The Buildkite job UUID. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
| `priority` | body | `string` | yes | The new priority for the job. |
