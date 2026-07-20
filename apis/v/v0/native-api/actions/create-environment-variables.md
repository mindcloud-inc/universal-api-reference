# Create Environment Variables with v0

Creates project environment variables in v0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectId/env-vars`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Create Environment Variables](https://v0.app/docs/api/platform/reference/projects/create-env-vars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ID of the project whose environment variables to create. |
| `environmentVariables[]` | body | `array<object>` | yes | — |
| `upsert` | body | `boolean` | no | — |
| `decrypted` | query | `boolean` | no | — |
