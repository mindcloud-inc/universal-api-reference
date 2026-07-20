# Update a project brief with Asana

Updates a project brief in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `project_briefs/:project_brief_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a project brief](https://developers.asana.com/reference/updateprojectbrief)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `string` | yes |
| `project_brief_gid` | path | `string` | yes |
