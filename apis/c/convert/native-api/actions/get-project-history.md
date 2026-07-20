# Get Project History with Convert

Retrieves project change history from Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:account_id/projects/:project_id/change-history`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Project History](https://api.convert.com/doc/v2/#tag/Projects/operation/getProjectHistory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
