# Create Project with Mendix

Creates a new project in Mendix and returns a job.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [Create Project](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the project. |
| `summary` | body | `string` | no | Description of the project. |
| `templateId` | body | `string` | no | Identifier of the template that the project will be copied from. If empty, Mendix uses the default template. |
| `image` | body | `string` | no | Base64-encoded project icon image. Mendix limits the file size and image dimensions. |
