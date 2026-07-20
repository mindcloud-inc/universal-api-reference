# Delete Annotation with Buildkite

Deletes a build annotation from Buildkite.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds/:build/annotations/:annotation`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Delete Annotation](https://buildkite.com/docs/apis/rest-api/annotations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotation` | path | `string` | yes | The Buildkite annotation UUID. |
| `build` | path | `string` | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
