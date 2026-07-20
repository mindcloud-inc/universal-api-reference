# Get Build Status with E2B

Retrieves template build status from E2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/{templateID}/builds/{buildID}/status`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Get Build Status](https://e2b.dev/docs/api-reference/templates/get-build-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buildID` | path | `string` | yes | Identifier of the template build. |
| `templateID` | path | `string` | yes | Identifier of the template. |
