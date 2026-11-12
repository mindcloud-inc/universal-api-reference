# Update Slides Position with Google Slides

Moves one or more slides to a new position in the presentation.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Update Slides Position](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#UpdateSlidesPositionRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[0].updateSlidesPosition.slideObjectIds[]` | body | `array<string>` | yes | IDs of the slides to move, in their current presentation order, without duplicates. |
| `requests[0].updateSlidesPosition.insertionIndex` | body | `number` | yes | Zero-based position to move the slides to, based on the order before the move. Must be between 0 and the slide count. |
