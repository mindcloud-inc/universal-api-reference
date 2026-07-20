# List Project Documents with Procore

Retrieves project folders and files from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2.0/projects/:project_id/documents`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Project Documents](https://developers.procore.com/reference/rest/documents#project-folder-and-file-index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
