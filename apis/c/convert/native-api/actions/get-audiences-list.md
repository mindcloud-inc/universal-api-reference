# List Audiences with Convert

Retrieves audiences from a Convert project.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:account_id/projects/:project_id/audiences`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [List Audiences](https://api.convert.com/doc/v2/#tag/Audiences/operation/getAudiencesList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
