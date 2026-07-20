# Get Screen Version with Zeplin

Retrieves a screen version from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/screens/{screen_id}/versions/{version_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Screen Version](https://docs.zeplin.dev/reference/getscreenversion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `version_id` | path | `string` | yes | Screen version id |
