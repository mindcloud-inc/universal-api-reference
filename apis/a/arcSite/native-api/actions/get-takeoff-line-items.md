# Get Takeoff Line Items with ArcSite

Retrieves takeoff line items from an ArcSite drawing.

## Endpoint

- **Method:** `GET`
- **Path:** `/drawings/:drawingId/takeoff_items`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Get Takeoff Line Items](https://dev.arcsite.com/#get-takeoff-line-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drawingId` | path | `string` | yes | The ID of the drawing. |
| `drawing_version_id` | query | `string` | no | The ID of the drawing version. |
