# Create a Project Revision with Jetbuilt

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:projectId/revisions`
- **Base URL:** `https://app.jetbuilt.com/api/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `projectId` | path | `string` | yes |
| `name` | body | `string` | no |
