# Create a project template from a project with Asana

Creates a project template from a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/saveAsTemplate`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a project template from a project](https://developers.asana.com/reference/projectsaveastemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.name` | body | `string` | yes | — |
| `data.public` | body | `boolean` | yes | — |
| `data.team` | body | `string` | yes | — |
| `data.workspace` | body | `string` | yes | — |
| `opt_fields[]` | query | `array<string>` | no | — |
| `project_gid` | path | `string` | yes | Path parameter: project_gid |
| `data` | body | `object` | yes | — |
