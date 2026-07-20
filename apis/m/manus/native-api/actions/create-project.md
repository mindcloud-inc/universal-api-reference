# Create Project with Manus

Creates a new project in Manus.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.manus.ai/v1`
- **Official documentation:** [Create Project](https://open.manus.ai/docs/v1/create-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the project |
| `instruction` | body | `string` | no | Default instruction applied to tasks in this project |
