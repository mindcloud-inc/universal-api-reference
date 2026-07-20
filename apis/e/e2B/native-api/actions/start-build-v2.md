# Start Build V2 with E2B

Starts a template build in E2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/templates/{templateID}/builds/{buildID}`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Start Build V2](https://e2b.dev/docs/api-reference/templates/start-build-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buildID` | path | `string` | yes | Identifier of the template build. |
| `templateID` | path | `string` | yes | Identifier of the template. |
