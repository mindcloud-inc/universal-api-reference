# Create Screenshot with Diffy

Creates a project screenshot in Diffy.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:id/screenshots`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Create Screenshot](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseUrl` | body | `string` | no | Base site URL for a custom environment. |
| `environment` | body | `string` | yes | Environment to capture: production, staging, development, or custom. |
| `id` | path | `number` | yes | Project ID. |
