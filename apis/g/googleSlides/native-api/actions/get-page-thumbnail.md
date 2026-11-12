# Get Page Thumbnail with Google Slides

Retrieves a page thumbnail URL from Google Slides.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/presentations/:presentationId/pages/:pageObjectId/thumbnail`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Get Page Thumbnail](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations.pages/getThumbnail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation. |
| `pageObjectId` | path | `string` | yes | The object ID of the page thumbnail to retrieve. |
