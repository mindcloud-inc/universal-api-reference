# List Drawing Areas with Procore

Retrieves drawing areas from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.1/projects/:project_id/drawing_areas`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Drawing Areas](https://developers.procore.com/reference/rest/drawing-areas#list-drawing-areas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
