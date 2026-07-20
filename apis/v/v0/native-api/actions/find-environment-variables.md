# Find Environment Variables with v0

Finds project environment variables in v0.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:projectId/env-vars`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Find Environment Variables](https://v0.app/docs/api/platform/reference/projects/find-env-vars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ID of the project whose environment variables to list. |
| `decrypted` | query | `boolean` | no | — |
