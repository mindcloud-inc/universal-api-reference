# Update Project with Planfix

Updates an existing project in Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:id`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Update Project](https://help.planfix.com/restapidocs/#/Project/post-project-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Planfix project identifier. |
| `name` | body | `string` | no | Updated project name. |
| `description` | body | `string` | no | Updated project description. |
