# Create Project with SimpleCert

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/new`
- **Base URL:** `https://app.simplecert.net/api`
- **Official documentation:** [Create Project](https://simplecert.readme.io/reference/projects-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `certificate` | body | `string` | yes | Certificate name to base the new project on. |
| `title` | body | `string` | yes | New project title. |
| `memo` | body | `string` | no | Project memo. |
