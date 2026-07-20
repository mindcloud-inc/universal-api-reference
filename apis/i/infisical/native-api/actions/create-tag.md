# Create Tag with Infisical

Creates a new tag for a project in Infisical.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/projects/:projectId/tags`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Create Tag](https://infisical.com/docs/api-reference/endpoints/secret-tags/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `slug` | body | `string` | yes |
| `color` | body | `string` | yes |
