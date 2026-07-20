# Get Project File URL with Frameshift

Retrieves a project file URL from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/files/:file_id/url`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Get Project File URL](https://mosaic.frameshift.io/api/#api-Project_Files-GetFile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `file_id` | path | `string` | yes | Resource identifier for the file to access |
| `create_activity` | query | `boolean` | no | If set to true will create a project activity |
