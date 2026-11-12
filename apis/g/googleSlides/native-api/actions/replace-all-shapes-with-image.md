# Replace All Shapes with Image with Google Slides

Replaces every shape that contains a given text with an image, useful for filling image placeholders in templates.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Replace All Shapes with Image](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#ReplaceAllShapesWithImageRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[0].replaceAllShapesWithImage.containsText` | body | `object` | no | — |
| `containsText.text` | body | `string` | yes | The text to search for in shapes and tables. |
| `containsText.matchCase` | body | `boolean` | no | Whether the search is case sensitive. |
| `containsText.searchByRegex` | body | `boolean` | no | Treat the search text as a regular expression; backslashes must be escaped. |
| `requests[0].replaceAllShapesWithImage.imageUrl` | body | `string` | yes | Public PNG, JPEG or GIF URL, at most 2 KB long. The image must be under 50 MB and 25 megapixels. |
| `requests[0].replaceAllShapesWithImage.imageReplaceMethod` | body | `list<string>` | no | Center Inside fits the image inside the shape keeping its aspect ratio; Center Crop fills the shape and may crop the image. Accepted values: `CENTER_CROP`, `CENTER_INSIDE`, `IMAGE_REPLACE_METHOD_UNSPECIFIED`. |
| `requests[0].replaceAllShapesWithImage.pageObjectIds[]` | body | `array<string>` | no | Limit the change to these slide IDs. Applies to all slides when empty. |
