# Delete Text with Google Slides

Deletes all or part of the text in a shape, text box, placeholder, or table cell.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/presentations/[:presentationId]\:batchUpdate`
- **Base URL:** `https://slides.googleapis.com`
- **API:** rest
- **Official documentation:** [Delete Text](https://developers.google.com/workspace/slides/api/reference/rest/v1/presentations/request#DeleteTextRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentationId` | path | `list<string>` | yes | The ID of the presentation to update. |
| `requests[0].deleteText.objectId` | body | `string` | yes | Object ID of the shape or table to delete text from. |
| `requests[0].deleteText.textRange` | body | `object` | no | — |
| `textRange.type` | body | `list<string>` | no | Fixed Range needs start and end index, From Start Index needs only start index, All needs neither. Accepted values: `ALL`, `FIXED_RANGE`, `FROM_START_INDEX`, `RANGE_TYPE_UNSPECIFIED`. |
| `textRange.startIndex` | body | `number` | no | Zero-based start of the range. |
| `textRange.endIndex` | body | `number` | no | Zero-based exclusive end of the range. Only for Fixed Range. |
| `requests[0].deleteText.cellLocation` | body | `object` | no | Only for table cells; Object ID must then be a table. |
| `cellLocation.rowIndex` | body | `number` | no | Zero-based row index. |
| `cellLocation.columnIndex` | body | `number` | no | Zero-based column index. |
