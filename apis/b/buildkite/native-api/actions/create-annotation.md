# Create Annotation with Buildkite

Creates a build annotation in Buildkite.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organization/pipelines/:pipeline/builds/:build/annotations`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Create Annotation](https://buildkite.com/docs/apis/rest-api/annotations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | The markdown body of the annotation. |
| `build` | path | `string` | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `context` | body | `string` | no | The annotation context label. |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
| `pipeline` | path | `string` | yes | The Buildkite pipeline slug. |
| `style` | body | `string` | no | The annotation style, such as success, info, warning, or error. |
