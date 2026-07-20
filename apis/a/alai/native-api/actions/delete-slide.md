# Delete Slide with Alai

Permanently deletes a slide from an Alai presentation.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/presentations/:presentation_id/slides/:slide_id`
- **Base URL:** `https://slides-api.getalai.com/api/v1`
- **Official documentation:** [Delete Slide](https://docs.getalai.com/api/delete-slide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentation_id` | path | `string` | yes | Target presentation identifier. |
| `slide_id` | path | `string` | yes | Slide identifier to delete. |
