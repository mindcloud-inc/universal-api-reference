# Create a project brief with Asana

Creates a project brief in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/project_briefs`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a project brief](https://developers.asana.com/reference/createprojectbrief)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `string` | yes |
| `project_gid` | path | `string` | yes |
