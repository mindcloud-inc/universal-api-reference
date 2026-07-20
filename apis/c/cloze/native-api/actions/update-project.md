# Update Project with Cloze

Updates a project in Cloze.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/update`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Update Project](https://api.cloze.com/api-docs/#/paths/v1-projects-update/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `direct` | body | `string` | no | Direct identifier for the project to update. |
| `name` | body | `string` | yes | Name of the project or deal. |
| `summary` | body | `string` | no | Summary description of the project or deal. |
| `appLinks[]` | body | `array<object>` | no | App links used to identify and merge the project. |
| `appLinks[].source` | body | `string` | no | App domain name for the app link. |
| `appLinks[].uniqueid` | body | `string` | no | Unique identifier within the app link source. |
