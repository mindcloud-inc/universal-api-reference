# Create Screen Version with Zeplin

Creates a new screen version in Zeplin.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/screens/{screen_id}/versions`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Create Screen Version](https://docs.zeplin.dev/reference/createscreenversion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `image` | body | `file` | yes | Binary data of the screen image. The image has to be in JPEG or PNG format, and its size cannot exceed 5MB. |
| `commit_message` | body | `string` | yes | Commit message for the screen version |
| `commit_color` | body | `string` | yes | Commit color for the screen version |
