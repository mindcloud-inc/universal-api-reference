# Create Screen with Zeplin

Creates a new screen in Zeplin.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/screens`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Create Screen](https://docs.zeplin.dev/reference/createscreen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `name` | body | `string` | yes | Name of the screen |
| `image` | body | `file` | yes | Binary data of the screen image. The image has to be in JPEG or PNG format, and its size cannot exceed 5MB. |
| `description` | body | `string` | yes | Description for the screen |
| `commit_message` | body | `string` | yes | Commit message for the screen version |
| `commit_color` | body | `string` | yes | Commit color for the screen version |
| `tags[]` | body | `array<string>` | yes | Tags for the screen |
| `section_id` | body | `string` | yes | Unique id of the screen section |
