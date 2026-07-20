# Get Build Logs with E2B

Retrieves logs for a template build from E2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/{templateID}/builds/{buildID}/logs`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Get Build Logs](https://e2b.dev/docs/api-reference/templates/get-build-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buildID` | path | `string` | yes | Identifier of the template build. |
| `templateID` | path | `string` | yes | Identifier of the template. |
