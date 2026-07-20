# Create Project with TickTick

Creates a new project in TickTick.

## Endpoint

- **Method:** `POST`
- **Path:** `/open/v1/project`
- **Base URL:** `https://api.ticktick.com`
- **Official documentation:** [Create Project](https://developer.ticktick.com/docs/index.html#/openapi?id=create-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Project name |
| `color` | body | `string` | no | Project color (hex) |
| `viewMode` | body | `string` | no | Project view mode |
| `kind` | body | `string` | no | Project kind |
| `sortOrder` | body | `number` | no | Project sort order |
