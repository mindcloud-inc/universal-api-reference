# Get Audience with Convert

Retrieves an audience from a Convert project.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/audiences/:audience_id`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Audience](https://api.convert.com/doc/v2/#tag/Audiences/operation/getAudience)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `audience_id` | path | `string` | yes | Convert audience ID. |
