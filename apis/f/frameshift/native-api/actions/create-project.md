# Create Project with Frameshift

Creates a new project in Frameshift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Create Project](https://mosaic.frameshift.io/api/#api-Projects-CreateProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the project to create |
| `reference` | body | `string` | no | The reference genome for the project. Required unless is_collection is true. |
| `description` | body | `string` | no | The details surrounding the project being created |
