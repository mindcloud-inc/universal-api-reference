# Create Project with Cloze

Creates a project in Cloze.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/create`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Create Project](https://api.cloze.com/api-docs/#/paths/v1-projects-create/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the project or deal. |
| `summary` | body | `string` | no | Summary description of the project or deal. |
| `stage` | body | `string` | no | Stage of the project. Accepted values: `0`, `1`, `2`, `3`. |
| `segment` | body | `string` | no | Segment of the project. |
| `appLinks[]` | body | `array<object>` | no | App links used to identify and merge the project. |
| `appLinks[].source` | body | `string` | no | App domain name for the app link. |
| `appLinks[].uniqueid` | body | `string` | no | Unique identifier within the app link source. |
