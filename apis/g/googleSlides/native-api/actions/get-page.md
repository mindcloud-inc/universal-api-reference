# Get Page with Google Slides

Retrieves a presentation page from Google Slides.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/presentations/:presentationId/pages/:pageObjectId`
- **Base URL:** `https://slides.googleapis.com`
- **Official documentation:** [Get Page](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations.pages/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `string` | yes | The ID of the presentation. |
| `pageObjectId` | path | `string` | yes | The object ID of the page to retrieve. |
