# Update Project Text Style with Zeplin

Updates an existing project text style in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/text_styles/{text_style_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Project Text Style](https://docs.zeplin.dev/reference/updateprojecttextstyle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `text_style_id` | path | `string` | yes | Text style id |
| `name` | body | `string` | yes | Name of the text style |
| `color` | body | `object` | yes | — |
