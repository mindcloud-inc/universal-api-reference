# Rebuild Build with Buildkite

Rebuilds an existing build in Buildkite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds/:build/rebuild`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Rebuild Build](https://buildkite.com/docs/apis/rest-api/builds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build` | path | `string` | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
