# Create Sample File with Frameshift

Creates a sample file in Frameshift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:project_id/samples/:sample_id/files`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Create Sample File](https://mosaic.frameshift.io/api/#api-Sample_Files-Create_Sample_File)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `sample_id` | path | `string` | yes | Resource identifier for the sample to access |
| `uri` | body | `string` | yes | The resource location of the file |
| `name` | body | `string` | yes | The name of the file |
| `reference` | body | `string` | yes | The genome build of the file |
| `type` | body | `string` | no | The file type of the file |
