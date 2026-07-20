# Update Project with Timing

Updates an existing project in Timing.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [Update Project](https://web.timingapp.com/docs/#projects-PUTapi-v1-projects--project_id-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Timing project ID to update. |
| `title` | body | `string` | no | — |
