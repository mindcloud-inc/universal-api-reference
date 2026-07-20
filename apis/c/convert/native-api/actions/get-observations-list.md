# List Observations with Convert

Retrieves observations from a Convert project.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:account_id/projects/:project_id/observations`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [List Observations](https://api.convert.com/doc/v2/#tag/Observations/operation/getObservationsList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
