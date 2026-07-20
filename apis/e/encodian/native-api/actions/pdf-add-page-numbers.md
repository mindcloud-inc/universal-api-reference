# PDF Add Page Numbers with Encodian

Adds page numbers to a PDF in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/AddPageNumbers`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Add Page Numbers](https://support.encodian.com/hc/en-gb/articles/360014464534)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filename` | body | `string` | yes | The PDF filename to be processed, including file extension. |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF document to be processed. |
| `StartPage` | body | `number` | no | Set which page to start adding page numbers from. |
| `StartNumber` | body | `number` | no | Set the starting number for the page numbers added to the document. |
| `PageNumberFormat` | body | `string` | no | Set the format of the page numbers added to the document. |
| `HorizontalAlignment` | body | `string` | no | Set the horizontal alignment of the page numbers added to the document. |
| `ReturnFile` | body | `boolean` | no | Sets whether the action should return a file or an operation ID. |
