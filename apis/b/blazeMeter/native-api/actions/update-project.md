# Update Project with BlazeMeter

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId`
- **Base URL:** `https:///a.blazemeter.com/api/v4`
- **Official documentation:** [Update Project](https://help.blazemeter.com/apidocs/#tag/projects/operation/projectsUpdateProject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
