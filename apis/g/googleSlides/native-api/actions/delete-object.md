# Delete Object with Google Slides

Deletes a slide or page element from a presentation.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Delete Object](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#DeleteObjectRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[0].deleteObject.objectId` | body | `string` | yes | Object ID of the slide or page element to delete. |
