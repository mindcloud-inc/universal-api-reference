# Get Drawing Payment with ArcSite

Retrieves payment details for one ArcSite drawing.

## Endpoint

- **Method:** `GET`
- **Path:** `/drawings/:drawingId/payment`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Get Drawing Payment](https://dev.arcsite.com/#get-drawing-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drawingId` | path | `string` | yes | The ID of the drawing. |
| `drawing_version_id` | query | `string` | no | The ID of the drawing version. |
