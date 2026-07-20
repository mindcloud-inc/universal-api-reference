# Get Drawing Location Photos with ArcSite

Retrieves location photos for one ArcSite drawing.

## Endpoint

- **Method:** `GET`
- **Path:** `/drawings/:drawingId/location_photos`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Get Drawing Location Photos](https://dev.arcsite.com/#get-drawing-location-photos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drawingId` | path | `string` | yes | The ID of the drawing. |
| `drawing_version_id` | query | `string` | no | The ID of the drawing version. |
