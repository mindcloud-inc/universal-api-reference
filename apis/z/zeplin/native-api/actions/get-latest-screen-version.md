# Get Latest Screen Version with Zeplin

Retrieves the latest screen version from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/screens/{screen_id}/versions/latest`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Latest Screen Version](https://docs.zeplin.dev/reference/getlatestscreenversion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
