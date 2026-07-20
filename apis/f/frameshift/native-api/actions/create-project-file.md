# Create Project File with Frameshift

Creates a project file in Frameshift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:project_id/files`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Create Project File](https://mosaic.frameshift.io/api/#api-Collections-Create_Project_File)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `uri` | body | `string` | yes | The resource location of the file |
| `name` | body | `string` | yes | The name of the file |
| `reference` | body | `string` | yes | The genome build of the file |
| `type` | body | `string` | no | The file type of the file |
