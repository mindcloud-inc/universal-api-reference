# Move Slide with Aspose

Moves a slide within a presentation in Aspose.

## Endpoint

- **Method:** `POST`
- **Path:** `/slides/:name/slides/:slideIndex/move`
- **Base URL:** `https://api.aspose.cloud/v3.0`
- **Official documentation:** [Move Slide](https://docs.aspose.cloud/slides/move-a-slide/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The presentation file name. |
| `slideIndex` | path | `number` | yes | The 1-based slide index to move. |
| `newPosition` | query | `number` | yes | The new 1-based slide position. |
