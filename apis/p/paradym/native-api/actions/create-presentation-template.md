# Create Presentation Template with Paradym

Creates a presentation template in Paradym.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/templates/presentations`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Create Presentation Template](https://paradym.id/reference#tag/presentation-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `credentials[0].type` | body | `string` | yes | The SD-JWT VC type to request in the presentation template. |
| `credentials[0].name` | body | `string` | no | Label for the requested credential in the template. |
| `credentials[0].description` | body | `string` | no | Description for the requested credential in the template. |
