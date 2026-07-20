# List Locations with Convert

Retrieves locations from a Convert project.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:account_id/projects/:project_id/locations`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [List Locations](https://api.convert.com/doc/v2/#tag/Locations/operation/getLocationsList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
