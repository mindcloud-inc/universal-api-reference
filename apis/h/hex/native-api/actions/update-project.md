# Update Project with Hex

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [Update Project](https://learn.hex.tech/docs/api-integrations/api/reference#operation/UpdateProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Unique ID for a Hex project. |
| `status` | body | `string` | no | Project status value. |
