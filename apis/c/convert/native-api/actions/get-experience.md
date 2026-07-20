# Get Experience with Convert

Retrieves an experience from a Convert project.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/experiences/:experience_id`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Experience](https://api.convert.com/doc/v2/#tag/Experiences/operation/getExperience)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `experience_id` | path | `string` | yes | Convert experience ID. |
