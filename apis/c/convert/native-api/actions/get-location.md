# Get Location with Convert

Retrieves a location from a Convert project.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/locations/:location_id`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Location](https://api.convert.com/doc/v2/#tag/Locations/operation/getLocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `location_id` | path | `string` | yes | Convert location ID. |
