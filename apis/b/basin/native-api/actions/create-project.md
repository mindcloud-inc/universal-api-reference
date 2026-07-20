# Create Project with Basin

Creates a new project in Basin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/projects/`
- **Base URL:** `https://usebasin.com`
- **Official documentation:** [Create Project](https://usebasin.com/api_docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `object` | no | Project fields to create. |
| `project.name` | body | `string` | yes | Project name. |
