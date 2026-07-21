# Create Project with BlazeMeter

Creates a project in BlazeMeter.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://a.blazemeter.com/api/v4`
- **Official documentation:** [Create Project](https://help.blazemeter.com/apidocs/#tag/projects/operation/projectsCreateProject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
