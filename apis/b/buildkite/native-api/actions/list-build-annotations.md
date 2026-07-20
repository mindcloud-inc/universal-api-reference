# List Build Annotations with Buildkite

Retrieves build annotations from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds/:build/annotations`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Build Annotations](https://buildkite.com/docs/apis/rest-api/annotations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build` | path | `string` | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
