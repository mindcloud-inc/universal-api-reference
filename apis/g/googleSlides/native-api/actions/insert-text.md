# Insert Text with Google Slides

Inserts text into a shape, text box, placeholder, or table cell on a slide.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Insert Text](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#InsertTextRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[0].insertText.objectId` | body | `string` | yes | Object ID of the shape or table to insert text into. |
| `requests[0].insertText.text` | body | `string` | yes | Text to insert. A newline starts a new paragraph. |
| `requests[0].insertText.insertionIndex` | body | `number` | no | Zero-based index, in Unicode code units, where the text is inserted. |
| `requests[0].insertText.cellLocation` | body | `object` | no | Only for table cells; Object ID must then be a table. |
| `cellLocation.rowIndex` | body | `number` | no | Zero-based row index. |
| `cellLocation.columnIndex` | body | `number` | no | Zero-based column index. |
