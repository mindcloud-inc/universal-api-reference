# Get Drawing with ArcSite

Retrieves one drawing by ID from ArcSite.

## Endpoint

- **Method:** `GET`
- **Path:** `/drawings/:drawingId`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Get Drawing](https://dev.arcsite.com/#get-drawing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drawingId` | path | `string` | yes | The ID of the drawing. |
| `drawing_version_id` | query | `string` | no | The ID of the drawing version. |
