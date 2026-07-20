# Create Project Color with Zeplin

Creates a new project color in Zeplin.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/colors`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Create Project Color](https://docs.zeplin.dev/reference/createprojectcolor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `name` | body | `string` | yes | Name of the color |
| `source_id` | body | `string` | yes | Color's identifier in the design tool |
| `r` | body | `number` | yes | Red component of the color |
| `g` | body | `number` | yes | Green component of the color |
| `b` | body | `number` | yes | Blue component of the color |
| `a` | body | `number` | yes | Alpha component of the color |
