# Update Dubbing Project with Murf Dub

Updates a dubbing project in Murf Dub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/murfdub/projects/:project_id/update`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [Update Dubbing Project](https://murf.ai/api/docs/api-reference/dubbing/projects/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Murf Dub project ID to update. |
| `target_locales[]` | body | `array<string>` | yes | Locales to keep on the project. |
