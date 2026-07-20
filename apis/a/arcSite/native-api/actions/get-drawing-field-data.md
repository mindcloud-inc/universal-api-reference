# Get Drawing Field Data with ArcSite

Retrieves field data values from an ArcSite drawing.

## Endpoint

- **Method:** `GET`
- **Path:** `/drawings/:drawingId/field_data`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Get Drawing Field Data](https://dev.arcsite.com/#get-drawing-field-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drawingId` | path | `string` | yes | The ID of the drawing. |
| `drawing_version_id` | query | `string` | no | The ID of the drawing version. |
