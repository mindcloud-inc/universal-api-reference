# Get Observation with Convert

Retrieves an observation from a Convert project.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/observations/:observation_id`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Observation](https://api.convert.com/doc/v2/#tag/Observations/operation/getObservation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `observation_id` | path | `string` | yes | Convert observation ID. |
