# Create Project with Timelink

Creates a project in the Timelink workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Create Project](https://api.timelink.io/documentation#/Projects/post_api_v1_projects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `client_id` | body | `string` | no |
| `ext_tool_id` | body | `string` | no |
