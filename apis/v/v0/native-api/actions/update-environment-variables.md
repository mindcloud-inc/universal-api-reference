# Update Environment Variables with v0

Updates project environment variables in v0.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/projects/:projectId/env-vars`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Update Environment Variables](https://v0.app/docs/api/platform/reference/projects/update-env-vars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ID of the project whose environment variables to update. |
| `environmentVariables[]` | body | `array<object>` | yes | — |
| `decrypted` | query | `boolean` | no | — |
