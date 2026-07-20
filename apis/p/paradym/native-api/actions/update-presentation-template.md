# Update Presentation Template with Paradym

Updates a presentation template in Paradym.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/templates/presentations/:presentationTemplateId`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Update Presentation Template](https://paradym.id/reference#tag/presentation-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationTemplateId` | path | `string` | yes | The presentation template ID. |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `credentials[0].type` | body | `string` | yes | The SD-JWT VC type to request in the presentation template. |
| `credentials[0].name` | body | `string` | no | Label for the requested credential in the template. |
| `credentials[0].description` | body | `string` | no | Description for the requested credential in the template. |
