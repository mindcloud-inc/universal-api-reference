# PDF Replace Text with Encodian

Replaces text in a PDF with Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/PdfSearchAndReplaceText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Replace Text](https://support.encodian.com/hc/en-gb/articles/15962260285980)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filename` | body | `string` | yes | The filename of the source PDF document including the file extension. |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the source PDF document. |
| `Phrases[]` | body | `array<object>` | yes | An array of phrases containing the search and replacement instructions. |
| `FinalOperation` | body | `boolean` | no | Set whether to return the file or just an operation ID. |
