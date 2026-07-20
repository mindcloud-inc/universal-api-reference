# List Project Files with Frameshift

Retrieves a list of project files from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/files`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [List Project Files](https://mosaic.frameshift.io/api/#api-Project_Files-Get_Project_Files)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `search` | query | `string` | no | The search keyword to filter the results by |
