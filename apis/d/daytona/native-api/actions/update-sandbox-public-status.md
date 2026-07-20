# Update Sandbox Public Status with Daytona

Updates the sandbox public status in Daytona.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandbox/[:sandboxIdOrName]/public/[:isPublic]`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Update Sandbox Public Status](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxIdOrName` | path | `string` | yes | Sandbox ID or name. |
| `isPublic` | path | `boolean` | yes | Whether the sandbox HTTP preview is publicly accessible. |
