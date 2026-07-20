# Create Project with Shuffll

Creates a new project in Shuffll.

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/project/create`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [Create Project](https://api-docs.shuffll.com/apis/projects/createproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | body | `string` | no | Optional output language. |
| `prompt` | body | `string` | yes | Project creation prompt. |
| `promptType` | body | `string` | no | Optional prompt type. |
| `toAutoEnhance` | body | `string` | no | Whether to auto enhance after project creation. |
| `toAutoExport` | body | `string` | no | Whether to auto export after project creation. |
| `videoLength` | body | `string` | no | Optional target video length in seconds. |
