# Update Screen with Zeplin

Updates an existing screen in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/screens/{screen_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Screen](https://docs.zeplin.dev/reference/updatescreen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `description` | body | `string` | yes | New description for screen |
| `tags[]` | body | `array<string>` | yes | New tags for the screen |
