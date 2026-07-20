# PDF Merge Files with Encodian

Merges PDF files in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/MergeArrayOfDocumentsToPdf`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Merge Files](https://support.encodian.com/hc/en-gb/articles/360014632213)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFilename` | body | `string` | yes | The filename to assign to the resulting PDF document including extension. |
| `documents[]` | body | `array<object>` | yes | JSON array containing a filename and base64 document content for each document to merge. |
| `generateBookmarks` | body | `boolean` | no | Generate a bookmark for each merged PDF document. |
| `pageNormalisation` | body | `boolean` | no | Normalise page width and height to the dimensions of the first file. |
| `preserveBookmarks` | body | `boolean` | no | Preserve bookmarks contained within each merged PDF document. |
| `removeMarkup` | body | `boolean` | no | Remove comments and tracked changes from Microsoft Office documents on conversion. |
| `pdfACompliant` | body | `boolean` | no | Set whether the resulting document should conform to PDF/A format. |
| `pdfAComplianceLevel` | body | `string` | no | Set the required level of PDF/A compliance. |
| `returnFile` | body | `boolean` | no | Set whether the action returns a file or an operation ID. |
