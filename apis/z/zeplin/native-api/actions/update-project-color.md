# Update Project Color with Zeplin

Updates an existing project color in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/colors/{color_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Project Color](https://docs.zeplin.dev/reference/updateprojectcolor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `color_id` | path | `string` | yes | Color id |
| `name` | body | `string` | yes | Name of the color |
| `r` | body | `number` | yes | Red component of the color |
| `g` | body | `number` | yes | Green component of the color |
| `b` | body | `number` | yes | Blue component of the color |
| `a` | body | `number` | yes | Alpha component of the color |
