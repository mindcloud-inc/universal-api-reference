# Create Project User with Viqeo

Creates a new project user in Viqeo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/media-platform/v1/project/:projectId/user`
- **Base URL:** `https://api.viqeo.tv`
- **Official documentation:** [Create Project User](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_e0bfa8f879)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project identifier from the path. |
| `email` | body | `string` | yes | User email address. |
| `locale` | body | `string` | yes | User locale, for example en. |
