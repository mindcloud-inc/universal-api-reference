# Convert File To PDF with Encodian

Converts a file to PDF in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/BasicConversion`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert File To PDF](https://support.encodian.com/hc/en-gb/articles/360011123574)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | A Base64 encoded representation of the file to be converted. |
| `outputFilename` | body | `string` | yes | The filename to assign to the resulting PDF document. |
| `filename` | body | `string` | yes | The filename, including the file extension, of the file to be converted. |
| `removeMarkup` | body | `boolean` | no | Sets whether comments and tracked changes should be removed from the document upon conversion. |
| `pdfACompliant` | body | `boolean` | no | Sets whether the resulting document should conform to PDF/A format. |
| `pdfAComplianceLevel` | body | `string` | no | Sets the required level of PDF/A compliance. |
| `generateBookmarks` | body | `boolean` | no | Set whether bookmarks should be automatically created for Microsoft Word documents that are converted to PDF. |
| `cultureName` | body | `string` | no | Set the culture for the documents prior to conversion. |
| `returnFile` | body | `boolean` | no | Sets whether the action should return a file or, alternatively, an operation ID. |
