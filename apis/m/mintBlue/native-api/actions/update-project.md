# Update Project with mintBlue

Updates an existing project in mintBlue.

## Endpoint

- **Method:** `POST`
- **Path:** `/sdk/latest`
- **Base URL:** `https://api.mintblue.com`
- **Official documentation:** [Update Project](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#updateProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.id` | body | `string` | yes | Project ID to update. |
| `params.data.name` | body | `string` | yes | Project name. |
| `params.data.description` | body | `string` | no | Optional project description. |
| `params.data.tags[]` | body | `array<string>` | no | Optional project tags. |
