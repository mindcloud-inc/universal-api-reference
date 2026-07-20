# List Drawings with Procore

Retrieves drawings from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.1/drawing_areas/:drawing_area_id/drawings`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Drawings](https://developers.procore.com/reference/rest/drawings#list-drawings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drawing_area_id` | path | `string` | yes | Unique identifier for the drawing area. |
