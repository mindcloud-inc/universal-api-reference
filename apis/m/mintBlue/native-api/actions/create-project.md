# Create Project with mintBlue

Creates a new project in mintBlue.

## Endpoint

- **Method:** `POST`
- **Path:** `/sdk/latest`
- **Base URL:** `https://api.mintblue.com`
- **Official documentation:** [Create Project](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#createProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.name` | body | `string` | yes | Project name. Prefer slug-style values (lowercase letters, numbers, hyphens), e.g. `codex-temp-20260402`, to avoid provider validation errors. |
| `params.description` | body | `string` | no | Optional project description. |
| `params.tags[]` | body | `array<string>` | no | Optional project tags. |
