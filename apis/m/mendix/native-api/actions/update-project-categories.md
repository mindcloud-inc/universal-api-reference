# Update Project Categories with Mendix

Updates project category assignments in Mendix.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [Update Project Categories](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project-id` | path | `string` | yes | The unique identifier of a project. |
| `categories[]` | body | `array<object>` | no | Array of project category assignments. Each item identifies a company category and the value to assign or clear. |
