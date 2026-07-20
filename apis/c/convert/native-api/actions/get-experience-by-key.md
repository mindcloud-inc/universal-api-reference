# Get Experience By Key with Convert

Retrieves an experience from Convert by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/experiences/:experience_key`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [Get Experience By Key](https://api.convert.com/doc/v2/#tag/Experiences/operation/getExperienceByKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
| `experience_key` | path | `string` | yes | Convert experience key. |
