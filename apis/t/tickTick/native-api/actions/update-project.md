# Update Project with TickTick

Updates an existing project in TickTick.

## Endpoint

- **Method:** `POST`
- **Path:** `/open/v1/project/:projectId`
- **Base URL:** `https://api.ticktick.com`
- **Official documentation:** [Update Project](https://developer.ticktick.com/docs/index.html#/openapi?id=update-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `list<string>` | yes | Project identifier |
| `name` | body | `string` | no | Project name |
| `color` | body | `string` | no | Project color (hex) |
| `viewMode` | body | `string` | no | Project view mode |
| `kind` | body | `string` | no | Project kind |
| `sortOrder` | body | `number` | no | Project sort order |
