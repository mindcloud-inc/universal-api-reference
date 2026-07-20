# Get Proposal Line Items with ArcSite

Retrieves proposal line items from an ArcSite drawing.

## Endpoint

- **Method:** `GET`
- **Path:** `/drawings/:drawingId/line_items`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Get Proposal Line Items](https://dev.arcsite.com/#get-proposal-line-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drawingId` | path | `string` | yes | The ID of the drawing. |
| `drawing_version_id` | query | `string` | no | The ID of the drawing version. |
